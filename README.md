# Act Two Expansion — Custom Campaign (Русская локализация)

Патч-мод с русским переводом для сюжетной модификации **[Act Two Expansion - Custom Campaign](https://www.nexusmods.com/baldursgate3/mods/24689)** для Baldur's Gate 3.

---

## О моде

**Act Two Expansion** расширяет сюжетную линию игры, добавляя масштабный новый регион между 2 и 3 актами со своими квестами, подземельями, диалогами, предметами и секретами.

Данный проект содержит файлы перевода текста на русский язык в виде отдельного зависимого мода локализации.

---

## Требования для игры

1. Установленная игра **Baldur's Gate 3** (актуальный официальный патч).
2. Оригинальный мод **[Act Two Expansion - Custom Campaign](https://www.nexusmods.com/baldursgate3/mods/24689)**.
3. **BG3 Mod Manager** (рекомендуется) или встроенный менеджер модов.

---

## Установка

1. Скачайте и установите оригинальный мод `ActTwoExpansion`.
2. Скачайте релизный `.pak` файл перевода из вкладки [Releases](https://github.com/adsyde/Act-Two-Expansion---Custom-Campaign-Russian/releases).
3. Поместите `.pak` в папку модов игры:
   `%LocalAppData%\Larian Studios\Baldur's Gate 3\Mods`
4. В менеджере модов расположите русификатор **строго ниже** оригинального мода:
   ```text
   [1] Act Two Expansion - Custom Campaign
   [2] Act Two Expansion - Russian Translation
   ```
5. Сохраните и экспортируйте порядок загрузки.

---

## Структура репозитория

```text
├── .claude/              # Настройки и правила для Claude Code
├── config/               # Конфигурация путей и параметров инструментов (Divine/LSLib)
├── data/                 # Канонические данные локализации (source, draft, approved в JSONL)
├── glossary/             # Терминологический словарь и стайлгайд
├── input/
│   ├── upstream/         # Оригинальные файлы мода (read-only)
│   └── extracted/        # Распакованные ресурсы
├── generated/            # Сформированные XML, meta.lsx и файлы перед упаковкой
├── releases/             # Готовые собранные .pak пакеты
├── reports/              # Отчеты валидации (QA, проверка токенов, покрытие)
├── scripts/              # Скрипты автоматизации (распаковка, сборка, QA)
├── CLAUDE.md             # Инструкции и правила для Claude Code
└── README.md             # Описание проекта
```

---

## Разработка и сборка

### Необходимые инструменты для сборки
- **Python 3.10+**
- **.NET 8 Runtime**
- **Divine CLI (LSLib)** от Norbyte
- **Claude Code** (Desktop или CLI)

### Основной цикл работы
1. **Синхронизация с оригиналом:** распаковка `.pak` и извлечение строк через `scripts/unpack.ps1`.
2. **Перевод и вычитка:** пакетная обработка строк через Claude Code с опорой на `glossary/glossary.csv`.
3. **QA-контроль:** запуск `scripts/qa.py` (контроль плейсхолдеров, целостности тегов и XML).
4. **Сборка пакета:** генерация `.loca` и сборка финального `.pak` через `scripts/build_mod.ps1`.
