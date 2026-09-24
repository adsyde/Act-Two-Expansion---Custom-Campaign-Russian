# Синхронизация с апстримом v0.8.0.5

Дата: 2026-09-24

## Изменения относительно предыдущего снимка

| Категория | Строк |
|---|---:|
| Новые | 6 |
| Изменился оригинал | 7 |
| Только version | 123 |
| Без изменений | 4857 |
| Исчезли из апстрима | 0 |
| Вернулись | 0 |

## Состояние памяти переводов

| Статус | Строк |
|---|---:|
| `approved` | 4767 |
| `do_not_translate` | 213 |
| `needs_review` | 7 |
| `untranslated` | 6 |

## Требуют вычитки (оригинал изменился)

- `h73f079d8g1946gff8aga8ffg36b8c34184c8` v3 -> v4
  - было:  `Once per battle, after your first cast of a Level 1 spell or higher, you can <LSTag Type="Spell" Tooltip="Projectile_Fly_TempestuousMagic">Fly</LSTag> as a <LSTag Tooltip="Bonus_Action">bonus action</LSTag> until the end of your turn without receiving <LSTag Tooltip="OpportunityAttack">Opportunity A`
  - стало: `Once per battle, after your first cast of a Level 1 spell or higher, you can <LSTag Type="Spell" Tooltip="Projectile_Fly_TempestuousMagic">Fly</LSTag> as a <lstag type="ActionResource" tooltip="BonusActionPoint">bonus action</lstag> until the end of your turn without receiving <LSTag Tooltip="Opport`
  - текущий перевод: `Раз за бой, после первого сотворенного заклинания 1-го круга или выше, вы можете <LSTag Type="Spell" Tooltip="Projectile_Fly_TempestuousMagic">Полететь</LSTag> <LSTag Tooltip="Bonus_Action">бонусным действием</LSTag> до конца своего хода, не вызывая <LSTag Tooltip="OpportunityAttack">атак по возможн`
- `hcebab782g8980g5bcag2543ga0627845ac0e` v2 -> v4
  - было:  `Enemies hit by throwing attacks with this weapon and are possibly knocked backed [1] and <LSTag Type="Status" Tooltip="STUNNED">Stunned</LSTag>. This has no effect on Huge creatures.`
  - стало: `Knock nearby foes <LSTag Type="Status" Tooltip="PRONE">Prone</LSTag> after killing a hostile target or landing a <LSTag Tooltip="CriticalHit">Critical Hit</LSTag>`
  - текущий перевод: `Враги, пораженные броском этого оружия, могут быть отброшены на [1] и <LSTag Type="Status" Tooltip="STUNNED">Оглушены</LSTag>. На Огромных существ не действует.`
- `ha61e028ag3e09g9372gb6e4g1c4f9dab1cf1` v2 -> v3
  - было:  `Gain an additional <LSTag Tooltip="StarMapPoint">Star Map Point</LSTag>`
  - стало: `Gain an additional <lstag type="ActionResource" tooltip="StarMapPoint">Star Map Point</lstag>.`
  - текущий перевод: `Вы получаете дополнительное <LSTag Tooltip="StarMapPoint">очко звездной карты</LSTag>`
- `h832fd81ege0ffgca1dg6ce6gd014508e4394` v12 -> v14
  - было:  `Where can I Nadine?`
  - стало: `Where can I find Nadine?`
  - текущий перевод: `Где мне найти Надин?`
- `h0038e872g5185g7898g16adg4409022fc719` v4 -> v5
  - было:  `Gain 7 <LSTag Tooltip="HitPoints">hit points</LSTag> and a <LSTag Tooltip="SuperiorityDie">Superiority Die</LSTag>.`
  - стало: `Gain 7 <LSTag Tooltip="HitPoints">hit points</LSTag> and a <lstag type="ActionResource" tooltip="SuperiorityDie">Superiority Die</lstag>.`
  - текущий перевод: `Вы получаете 7 <LSTag Tooltip="HitPoints">ОЗ</LSTag> и <LSTag Tooltip="SuperiorityDie">кость превосходства</LSTag>.`
- `h02e6a0cegc7f6g9681g47d4g93310903ee64` v2 -> v3
  - было:  `Once per combat, gain an additional <LSTag Type="ActionResource" Tooltip="ActionPoint">action</LSTag> after killing a hostile creature.`
  - стало: `Once per turn, gain an additional <LSTag Type="ActionResource" Tooltip="BonusActionPoint">bonus action</LSTag> after killing a hostile creature.`
  - текущий перевод: `Раз за бой: убив враждебное существо, вы получаете дополнительное <LSTag Type="ActionResource" Tooltip="ActionPoint">действие</LSTag>.`
- `h9b7d73bfg4af4g98fagd7d6g1c7671abc9fd` v2 -> v4
  - было:  `Explore the Sunrise Spire Vaults`
  - стало: `Investigate the Prayer Room in the Sunrise Spire Vaults further`
  - текущий перевод: `Исследовать хранилища Шпиля Рассвета`

## Новые строки (первые 50)

- `h2f9f2bbcg6616g530dgd916gf6af21d6dc34` — Eladrin
- `h7131ba7eg33a0g4aceg1ff2ga79ac7d3882a` — Eladrin are elves native to the Feywild and reflect it in every way - beautiful, unpredictable, and capable of harnessing boundless magic.
- `hd0135141g3291gfafcgbeaeg22121be91a48` — Shadar-Kai
- `h32b8210cgd650g51f9g3c49gee5478d7adf5` — With ethereal countenances and long lifespans, elves are at home with nature's power, flourishing in light and dark alike.
- `h84c3c1c9g2feega7a2g8f3fgd717eadac5b6` — Heroic Throw
- `hb0895a3dgb381g5c47gab53g5f63b5b586f0` — Throw the Breacher, causing it to explode on impact, pushing targets back [1].
