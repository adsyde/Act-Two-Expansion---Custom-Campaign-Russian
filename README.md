![Act Two Expansion - Custom Campaign Russian](images/24689_1788047926.webp)

# Act Two Expansion — русская локализация

Патч-перевод мода [Act Two Expansion - Custom Campaign](https://www.nexusmods.com/baldursgate3)
для Baldur's Gate 3. Репозиторий рассчитан на **повторяющийся цикл**: мод
обновляется, перевод досинхронизируется, ничего из сделанного не теряется.

Текущая версия апстрима: **0.8** (4987 строк).

Состояние перевода: **1402 строки (28.1%)** готовы и входят в сборку.
Непереведенные строки игра показывает по-английски.

## Быстрый старт

```powershell
# 1. Разовая настройка
copy config\tools.local.example.json config\tools.local.json   # укажите путь к Divine.exe
# положите .pak мода в input\upstream\ и пропишите его в config\tools.json

# 2. Подготовка данных
scripts\unpack.ps1
python scripts\extract_strings.py
python scripts\sync.py

# 3. Перевод
python scripts\make_batch.py --limit 50
#    заполнить target и выставить status=approved в data\batches\batch_NNN.jsonl
python scripts\merge_batch.py data\batches\batch_NNN.jsonl

# 4. Сборка
scripts\build_mod.ps1 -Version "0.1.0"
```

Подробности, включая процедуру обновления на новую версию мода, —
**[docs/WORKFLOW.md](docs/WORKFLOW.md)**.

## Скрипты

| Скрипт | Назначение |
|---|---|
| `unpack.ps1` | распаковка `.pak` апстрима, декодирование `.loca` → `.xml`, фиксация SHA256 |
| `extract_strings.py` | снимок английских строк → `data/source.en.jsonl` |
| `sync.py` | сверка снимка с памятью переводов, отчет об изменениях |
| `make_batch.py` | нарезка работы на батчи |
| `merge_batch.py` | возврат батча в память + размножение перевода на дубликаты |
| `qa.py` | контроль качества, блокирует сборку при ошибках |
| `generate_xml.py` | русский XML локализации |
| `generate_meta.py` | `meta.lsx` мода-перевода |
| `build_mod.ps1` | QA → XML → `.loca` → `.pak` |
| `config_get.py` | чтение объединенного конфига (используется из `.ps1`) |

## Требования

- Windows, PowerShell 5.1+
- Python 3.9+
- [LSLib](https://github.com/Norbyte/lslib) (`Divine.exe`) — путь указывается
  в `config/tools.local.json`

## Правила работы

Подробности процесса — [docs/WORKFLOW.md](docs/WORKFLOW.md), терминология —
[glossary/](glossary/). Ключевое:

- `input/upstream/` неприкосновенен;
- `contentuid` и `version` не генерируются и не меняются;
- плейсхолдеры и теги `<LSTag>`, `<br>`, `<font>` сохраняются без изменений,
  включая атрибуты — это проверяет `qa.py`;
- терминология сверяется с `glossary/glossary.csv` и официальной русской
  локализацией BG3.
