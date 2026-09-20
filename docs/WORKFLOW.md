# Рабочий процесс

## Схема данных

```
input/upstream/*.pak            READ-ONLY, в git не попадает (чужой контент, сотни МБ)
        │ scripts/unpack.ps1
input/extracted/<версия>/       распаковка, в git не попадает
        │ scripts/extract_strings.py
data/source.en.jsonl            снимок английского текста текущей версии (производный,
        │                       перезаписывается, руками не редактируется)
        │ scripts/sync.py
data/translations.jsonl   <---- ЕДИНСТВЕННЫЙ ИСТОЧНИК ПРАВДЫ: переводы + статусы + история
        │ scripts/make_batch.py          ^
data/batches/batch_NNN.jsonl               │ scripts/merge_batch.py
        │ (перевод)  ────────────────────-─┘
        │ scripts/generate_xml.py + generate_meta.py
build/ + package/               промежуточная сборка, в git не попадает
        │ scripts/build_mod.ps1
releases/*.pak                  готовый мод-перевод
```

`data/translations.jsonl` переживает обновления мода: переводы не теряются
никогда, даже если строка временно исчезла из апстрима.

## Статусы строки

| Статус | Значение | Идет в .pak |
|---|---|---|
| `untranslated` | перевода нет | нет |
| `needs_context` | контекст неясен, `target` пустой (CLAUDE.md §4) | нет |
| `translated` | перевод есть, не вычитан | только с `-IncludeTranslated` |
| `approved` | вычитан | **да** |
| `needs_review` | английский оригинал изменился, старый перевод сохранен | нет |
| `obsolete` | строки больше нет в апстриме, перевод лежит в памяти | нет |

Непереведенные строки в русский `.loca` не попадают — игра берет для них
английский текст из оригинального мода. Поэтому частичный перевод безопасен
и его можно выпускать в любой момент.

---

## Сценарий А. Обычный рабочий цикл (перевод текущей версии)

```powershell
python scripts\make_batch.py --limit 50          # нарезать следующую порцию
# ... заполнить target и выставить status=approved в data/batches/batch_NNN.jsonl
python scripts\qa.py data\batches\batch_NNN.jsonl # проверить батч до слияния
python scripts\merge_batch.py data\batches\batch_NNN.jsonl
python scripts\qa.py
```

Полезные варианты нарезки:

```powershell
python scripts\make_batch.py --max-len 40 --limit 100      # короткие: предметы, имена, UI
python scripts\make_batch.py --filter "LSTag" --limit 30   # описания способностей
python scripts\make_batch.py --status needs_review         # вычитка после обновления мода
```

`merge_batch.py` распространяет перевод на все строки с идентичным
английским оригиналом. В моде ~3200 повторов на 4987 строк, поэтому
переведенные 40 строк закрыли сразу 179.

---

## Сценарий Б. Вышла новая версия мода

1. Положить новый `.pak` в `input/upstream/`.
2. В `config/tools.json` обновить `upstream.version` и `upstream.pak`
   (если поменялось имя файла или UUID-папка — то и `mod_folder`/`mod_uuid`).
3. Выполнить:

```powershell
scripts\unpack.ps1
python scripts\extract_strings.py
python scripts\sync.py
```

`sync.py` сравнит новый снимок с памятью переводов и напишет отчет
`reports/sync_<версия>.md`:

| Категория | Что делает sync |
|---|---|
| новые строки | заводит записи со статусом `untranslated` |
| изменился английский текст | ставит `needs_review`, **сохраняет старый перевод** и записывает `prev_source` для сравнения |
| сменилась только `version` | обновляет номер, статус не трогает |
| строка исчезла из апстрима | ставит `obsolete`, перевод сохраняется |
| строка вернулась | восстанавливает прежний статус |

4. Разобрать работу: сначала вычитка изменившегося, потом новое.

```powershell
python scripts\make_batch.py --status needs_review --limit 100
python scripts\make_batch.py --status untranslated --limit 100
```

5. Собрать релиз (см. ниже). Версия апстрима попадает в имя `.pak`,
   поэтому релизы под разные версии мода не перепутать.

---

## Сценарий В. Сборка релиза

```powershell
scripts\build_mod.ps1 -Version "0.2.0"
```

Скрипт по шагам: QA (блокирует сборку при ошибках) -> русский XML ->
`meta.lsx` -> компиляция `.loca` -> `.pak` -> печать состава пакета.

Состав итогового пакета:

```
Mods/<UUID-папка оригинального мода>/Localization/Russian/ActTwoExpansion.loca
Mods/ActTwoExpansion_Russian/meta.lsx
```

Русский `.loca` лежит **внутри папки оригинального мода** — иначе игра его
не найдет. `meta.lsx` — в собственной папке, чтобы перевод был отдельным
модом в списке загрузки. В зависимостях объявлен оригинальный мод с пустым
`MD5`: так перевод не ломается при обновлении апстрима.

Флаги:

- `-IncludeTranslated` — включить невычитанные строки (для тестовых сборок).
- `-SkipQa` — только для отладки, публиковать такую сборку нельзя.

---

## Установка тестовой сборки

1. Скопировать `.pak` из `releases/` в
   `%LOCALAPPDATA%\Larian Studios\Baldur's Gate 3\Mods`.
2. Включить мод в менеджере модов **после** оригинального Act Two Expansion.
3. Язык игры — русский.

## Что и почему не в git

| Путь | Причина |
|---|---|
| `input/upstream/*`, `input/extracted/` | чужой контент, сотни МБ |
| `config/*.local.json` | локальные пути (LSLib, папка игры) — у каждого свои |
| `scripts/local/` | личные скрипты запуска/копирования |
| `build/`, `package/`, `releases/` | производные артефакты |

Машинные пути задаются в `config/tools.local.json` — шаблон лежит в
`config/tools.local.example.json`.
