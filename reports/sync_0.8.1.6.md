# Синхронизация с апстримом v0.8.1.6

Дата: 2026-11-01

## Изменения относительно предыдущего снимка

| Категория | Строк |
|---|---:|
| Новые | 2 |
| Изменился оригинал | 2 |
| Только version | 88 |
| Без изменений | 5043 |
| Исчезли из апстрима | 0 |
| Вернулись | 0 |

## Состояние памяти переводов

| Статус | Строк |
|---|---:|
| `approved` | 4922 |
| `do_not_translate` | 213 |

## Требуют вычитки (оригинал изменился)

- `ha1430177g26b5ga755g6b3cg59279d62fd34` v96 -> v100
  - было:  `The wild magic here allows me to speak with them in way but I cannot command them. The forest rises up in vengeance against all preceived invaders. Stay safe out there.`
  - стало: `The wild magic here allows me to speak with them in way but I cannot command them. The forest rises up in vengeance against all perceived invaders. Stay safe out there.`
  - текущий перевод: `Здешняя дикая магия отчасти позволяет мне говорить с ними, но приказывать я им не могу. Лес поднимается, чтобы отомстить всякому, кого считает захватчиком. Берегите себя.`
- `h02e6a0cegc7f6g9681g47d4g93310903ee64` v3 -> v4
  - было:  `Once per turn, gain an additional <LSTag Type="ActionResource" Tooltip="BonusActionPoint">bonus action</LSTag> after killing a hostile creature.`
  - стало: `Once per battle, after killing a hostile creature, gain an additional <LSTag Type="ActionResource" Tooltip="BonusActionPoint">bonus action</LSTag> that round.`
  - текущий перевод: `Раз за ход: убив враждебное существо, вы получаете дополнительное <LSTag Type="ActionResource" Tooltip="BonusActionPoint">бонусное действие</LSTag>.`

## Итог после вычитки и аудита вне локализации

4922 approved, 213 do_not_translate; незавершенных переводов нет. Две строки
оригинала вычитаны батчем `batch_0816_update.jsonl`. Описание бонусного действия
обновлено, исправление perceived не меняет смысл русского перевода.

Аудит выявил два ключа кнопок OpenMessageBoxChoice, использованные и ранее,
а теперь также в новой развилке завершения акта. Они добавлены в снимок как
производные choice_alias и переведены батчем `batch_0816_choices.jsonl`.
Новые строки english.xml отсутствуют; 2 новых записи — покрытие вне loca.

- `h4a2fc48dge4a7g5935gb754gafdddf567cd9` — Return
- `h7f7b242egbf87g59d7gbb61g1a4834354b91` — Venture Forth

Таблица выше объединяет обе синхронизации относительно резервной копии до
обновления. Исходные логи обеих операций сохранены в work/E01/logs/update-0816.
