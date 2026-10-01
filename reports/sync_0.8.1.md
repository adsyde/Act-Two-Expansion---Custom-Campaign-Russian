# Синхронизация с апстримом v0.8.1

Дата: 2026-10-01

## Изменения относительно предыдущего снимка

| Категория | Строк |
|---|---:|
| Новые | 99 |
| Изменился оригинал | 35 |
| Только version | 146 |
| Без изменений | 4812 |
| Исчезли из апстрима | 0 |
| Вернулись | 0 |

## Состояние памяти переводов

| Статус | Строк |
|---|---:|
| `approved` | 4745 |
| `do_not_translate` | 213 |
| `untranslated` | 99 |
| `needs_review` | 35 |

## Требуют вычитки (оригинал изменился)

- `h92d07478gbd68g4d11gf1aeg907dcc7d1431` v6 -> v7
  - было:  `Once per battle, when a creature deals melee damage to the wearer, that creature takes [1] and is <LSTag Type="Status" Tooltip="POISONED">Poisoned</LSTag> for 2 turns.`
  - стало: `Once per battle, when a creature deals melee damage to the wearer, that creature takes [1] and is possibly <LSTag Type="Status" Tooltip="POISONED">Poisoned</LSTag> for 2 turns.`
  - текущий перевод: `Раз за бой: когда существо наносит носителю урон в ближнем бою, оно получает [1] и <LSTag Type="Status" Tooltip="POISONED">Отравление</LSTag> на 2 хода.`
- `hf1a4ca7cg4914g4c37gd925gf5a6306321d7` v6 -> v7
  - было:  `Once per <LSTag Tooltip="ShortRest">Short Rest</LSTag>, when a creature critically strikes you with a melee attack, you become <LSTag Type="Spell" Tooltip="Target_Invisibility">Invisible</LSTag> for 1 turn.`
  - стало: `Once per combat, when a creature critically strikes you with a melee attack, you become <LSTag Type="Spell" Tooltip="Target_Invisibility">Invisible</LSTag> for 2 turns.`
  - текущий перевод: `Раз за <LSTag Tooltip="ShortRest">Короткий отдых</LSTag>: когда существо наносит вам критический удар в ближнем бою, вы становитесь <LSTag Type="Spell" Tooltip="Target_Invisibility">Невидимым</LSTag> на 1 ход.`
- `h5f04eae6gcbffg3ee5g126fg13f3800f4dd5` v8 -> v10
  - было:  `A journal, alongside a key, belonging to the lord of Sunrise Vineyard mentions a hidden vault beneath the manor. It is accessible through the cellar using an “old gnomish trick”. We should check it out.`
  - стало: `A journal, alongside a key, belonging to the lord of Sunrise Vineyard mentions a hidden vault beneath the manor. It is hidden in the cellar using an “old gnomish trick”. We should check it out.`
  - текущий перевод: `Дневник и ключ, принадлежавшие лорду Виноградника Рассвета, упоминают тайное хранилище под усадьбой. Попасть туда можно через погреб, используя «старый гномий прием». Стоит проверить.`
- `h2c923af2g75d2gd3afgb3bfg35c0f7058b36` v1 -> v2
  - было:  `Steel Grip`
  - стало: `Iron Grip`
  - текущий перевод: `Стальная хватка`
- `h0d61f886g67f3g0b2dg5f6cge2a2609a0a91` v33 -> v34
  - было:  `A pleasure. My name is Altan, and over there is Leigh. We're merchants with the Zhentarim, and as luck would have it, we're open for business a little longer than expected after our boat was attacked.`
  - стало: `A pleasure. My name is Altan, and over there is Leigh. We're merchants by trade, and as luck would have it, we're open for business a little longer than expected after our boat was attacked.`
  - текущий перевод: `Рад знакомству. Меня зовут Алтан, а вон там — Ли. Мы торговцы из Жентарима и, по счастливой случайности, задержались с торговлей дольше, чем рассчитывали: на нашу лодку напали.`
- `h6652cbadg2da6g6ed3geb5cg060dd9ed461e` v26 -> v52
  - было:  `[Disrupt the ritual]`
  - стало: `[Remove the idol]`
  - текущий перевод: `[Прервать ритуал]`
- `h3af42794gc0e0g96f6gdea0gdc0d57f182ec` v6 -> v8
  - было:  `Find a use for the Nexus Stone`
  - стало: `Search the Anga Vled Mines for a hidden chamber`
  - текущий перевод: `Найти применение Камню Узла`
- `hf9b2fba4g97c7g35c0g5584g216f942bfb21` v4 -> v6
  - было:  `We found a peculiar gemstone locked inside a vault under the Sunrise Vineyard manor. It might be useful.`
  - стало: `We found a peculiar gemstone, alongside a note, that mentions it was taken from a secret chamber in the Anga Vled Mines. There could be more to this.`
  - текущий перевод: `Мы нашли необычный самоцвет, запертый в хранилище под усадьбой Виноградника Рассвета. Возможно, он пригодится.`
- `hf4ac0a99g1f9agde79gb8f5gcc9713628a66` v6 -> v8
  - было:  `We opened the sealed door to the druid sanctum. We can now find out what's inside.`
  - стало: `We discovered an ancient druid sanctum in the Shadow-Cleansed Lands. We should see what we can find inside.`
  - текущий перевод: `Мы открыли запечатанную дверь в святилище друидов. Теперь можно выяснить, что внутри.`
- `hd0119b3eg0a99g8c43g6a76ge40dd0aabd51` v71 -> v73
  - было:  `Sprawling vines bar the way into a ruin.`
  - стало: `Sprawling vines bar the way into a room.`
  - текущий перевод: `Разросшиеся лозы преграждают путь в руины.`
- `h8fe1f88dga565g5d62gd617g74273f55e12b` v71 -> v76
  - было:  `Try to command the vines to rescind.`
  - стало: `Command the vines to rescind.`
  - текущий перевод: `Попытаться приказать лозам отступить.`
- `he8d2272cgcda3g8aedgcf00gb3d961febafa` v62 -> v67
  - было:  `Try to command the vines to rescind.`
  - стало: `Command the vines to rescind.`
  - текущий перевод: `Попытаться приказать лозам отступить.`
- `h557f00f1g9951g0e33gae87gd0f3db383771` v4 -> v6
  - было:  `We found a crystal mechanism in a hidden chamber beneath Sunrise Spire. We should investigate it.`
  - стало: `We found a crystal mechanism in a hidden chamber beneath Sunrise Spire. We should find out what it does.`
  - текущий перевод: `Мы нашли кристаллический механизм в скрытом зале под Шпилем Рассвета. Стоит его осмотреть.`
- `h64c493beg3037gc1e1g2d9bgf905baa19bfb` v2 -> v4
  - было:  `We activated the crystal mechanism beneath Sunrise Spire. There may be more to this contraption. We should keep exploring.`
  - стало: `We activated the crystal mechanism beneath Sunrise Spire. We should find out what exactly it did.`
  - текущий перевод: `Мы запустили кристаллический механизм под Шпилем Рассвета. Возможно, в этом устройстве есть что-то еще. Стоит продолжить поиски.`
- `hfb46af5eg23a7g9fdfg9701g9fbd31ae6439` v57 -> v62
  - было:  `These vines are enchanted with ancient druidic magic. It's possible that the druids had a method or item to allow themselves to bypass the barrier freely.`
  - стало: `These vines are enchanted with ancient druidic magic. It's possible that the druids had a magical item to allow themselves to bypass the barrier freely.`
  - текущий перевод: `Эти лозы зачарованы древней друидической магией. Возможно, у друидов был способ или предмет, позволявший свободно проходить через преграду.`
- `h38c89819g5fbdg3b4cg3eacg1d90f6959c03` v5 -> v7
  - было:  `The Mind Killer`
  - стало: `Phasmid Longbow`
  - текущий перевод: `Убийца Разума`
- `h8bfb7d97g0011gb303ga169g72fe891f1622` v2 -> v3
  - было:  `Use a reaction to strike a foe that just missed you with an unarmed attack and slightly knock them back.`
  - стало: `Use a reaction to strike a foe that just missed you with an unarmed attack and shoving them back.`
  - текущий перевод: `Реакцией ударьте безоружной атакой врага, только что по вам промахнувшегося, и слегка отбросьте его.`
- `h61b1134cgd4e9g8835gb375g633419f16b02` v4 -> v6
  - было:  `We replaced the crystal in the device at the top of Sunrise Spire but we still can't activate the device. We should keep investigating Sunrise Spire for clues.`
  - стало: `We replaced the crystal in the device at the top of Sunrise Spire but we still can't activate the device. We should keep investigating the Sunrise Spire Vaults for clues.`
  - текущий перевод: `Мы заменили кристалл в устройстве на вершине Шпиля Рассвета, но включить его по-прежнему не удается. Стоит поискать подсказки дальше по Шпилю Рассвета.`
- `h857fd063g6be4g1b48g38a9gaefe02519d5b` v21 -> v25
  - было:  `Nothing happens. Something must be missing.`
  - стало: `Nothing happens even with the crystal in place. There must be more involved to power it up.`
  - текущий перевод: `Ничего не происходит. Чего-то не хватает.`
- `h1d55d7a1g4357g8ccdgfd95gf33b3f1cccd0` v43 -> v48
  - было:  `These vines are enchanted with ancient druidic magic. It's possible that the druids had a method or item to allow themselves to bypass the barrier freely.`
  - стало: `These vines are enchanted with ancient druidic magic. It's possible that the druids had a magical item to allow themselves to bypass the barrier freely.`
  - текущий перевод: `Эти лозы зачарованы древней друидической магией. Возможно, у друидов был способ или предмет, позволявший свободно проходить через преграду.`
- `h4f4bc1aag8f40ge63fgc55cgf4d7f7cc38ea` v2 -> v4
  - было:  `We opened the way to a prayer room in the Sunrise Spire Vaults. There may be more to this chamber than meets the eye.`
  - стало: `We found a prayer room locked behind a door in the Sunrise Spire Vaults. There may be more to this chamber than meets the eye.`
  - текущий перевод: `Мы открыли путь в молельню в хранилищах Шпиля Рассвета. Возможно, в этом зале есть больше, чем кажется на первый взгляд.`
- `h4f1a755dg8925g7227g2814gaa9fd7e1b505` v12 -> v38
  - было:  `Try to determine the ritual that took place here`
  - стало: `[Try to determine the ritual that took place here]`
  - текущий перевод: `Попытаться понять, какой ритуал здесь провели`
- `hdf508d20g8546g38d7gec93g8bdd145d13f9` v12 -> v38
  - было:  `(Leave)`
  - стало: `<i>Leave.</i>`
  - текущий перевод: `(Уйти)`
- `hf02caec2g2fe3g2c14g0cfcg344df2dc3f0a` v12 -> v38
  - было:  `This Idol of Silvanus was used to conduct the Rite of Thorns. The magical vines and guardians still protecting this place awakened here long ago.`
  - стало: `*This Idol of Silvanus was used to conduct the Rite of Thorns. Disturbing it is sure to awaken the ancient defenses it still empowers.*`
  - текущий перевод: `Этим идолом Сильвануса проводили Обряд Шипов. Магические лозы и стражи, что до сих пор охраняют это место, пробудились здесь давным-давно.`
- `h8dd66ccege61dgc0e6gd015g3b81213f4109` v12 -> v38
  - было:  `It's unclear to you what ritual the idol was used for.`
  - стало: `*It's unclear to you what the idol is being used for.*`
  - текущий перевод: `Для какого ритуала использовали идола, вам не ясно.`
- `haa8f65cegfa98g17bag0f7fgd36eb65db818` v31 -> v36
  - было:  `Sprawling vines bar the way into a druidic ruin.`
  - стало: `Living vines bar the way into a room.`
  - текущий перевод: `Разросшиеся лозы преграждают путь в друидические руины.`
- `hbe2d4f81g3014g17a1g8213g3358a9ebe206` v4 -> v6
  - было:  `We found a Sun Crystal on the corpse of a Sun Soul Monk in the Sunrise Spire Vaults. His journal mentions using the crystal to restore the spire. It might be worth finding a way to access the spire.`
  - стало: `We found a Sun Crystal on the corpse of a Sun Soul Monk in the Sunrise Spire Vaults. His journal mentions using the crystal to restore the spire. The journal mentions that the way to the spire might be accessed through the Sunrise Spire Vaults.`
  - текущий перевод: `В хранилищах Шпиля Рассвета мы нашли солнечный кристалл на теле монаха Солнечной души. В его дневнике сказано, что кристаллом можно восстановить шпиль. Возможно, стоит найти путь наверх.`
- `hfa0a95d3g78d4g9221g751fgeeff6b051ebe` v30 -> v46
  - было:  `We could help you restore Sunrise Spire.`
  - стало: `We could help you restore Sunrise Spire. What must we do?`
  - текущий перевод: `Мы могли бы помочь тебе восстановить Шпиль Рассвета.`
- `h2ec0ba7dg1fabgee7ag4f7bgac25d963af30` v30 -> v46
  - было:  `We are an ancient Order that worships Lathander, Selûne, and Sune. Many would find our old beliefs heretical, but we are simply trying to do good where we can.`
  - стало: `We are an ancient Order that worships Lathander, Selûne, and Sune. Some would find our old beliefs heretical, but we are simply trying to do good where we can.`
  - текущий перевод: `Мы — древний орден, чтущий Латандера, Селунэ и Суну. Многим наши старые верования покажутся ересью, но мы просто стараемся творить добро там, где можем.`
- `hfb70b80agfbe9gb513g6784g19196818601d` v30 -> v46
  - было:  `By placing this gem at the top of the spire. The problem is I haven't found a way there. The doors at the end of the hall are locked. The key might be in the library, but I've heard strange noises coming from there.`
  - стало: `I've been entrusted with a Sun Crystal meant to restore the one missing here. The problem has been finding out where exactly it goes.`
  - текущий перевод: `Нужно поместить этот самоцвет на вершину шпиля. Беда в том, что пути наверх мне найти не удалось. Двери в конце зала заперты. Ключ может быть в библиотеке, но оттуда доносятся странные звуки.`
- `hb9473bf6g31b6g780dge092gc9afc3cafd49` v30 -> v46
  - было:  `Most died fighting the cult. We tried too many times to be heroes. And as the Absolute's influence spread, we found ourselves outnumbered and outmatched.`
  - стало: `We tried too many times to be heroes and paid with our blood. And as the Absolute's influence spread, we found ourselves further outnumbered and outmatched.`
  - текущий перевод: `Большинство погибло в боях с культом. Мы слишком часто пытались быть героями. А когда влияние Абсолют разрослось, нас стало меньше и мы оказались слабее.`
- `hec726aa6g16bcg608dgceacgd194c2e0f167` v30 -> v46
  - было:  `With my fellows gone, it seems I have little choice than to put my trust in strangers. I was never the fighter of the group.`
  - стало: `With my fellows gone, it seems I have little choice than to put my trust in strangers. Very well. Take this Sun Crystal and find out how to activate the spire with it.`
  - текущий перевод: `Раз моих товарищей больше нет, похоже, выбора нет — придется довериться чужакам. Боец из меня всегда был никудышный.`
- `h4f5a3dfeg120fge32cg9200ge34ec1a0bd87` v2 -> v4
  - было:  `We met a Sun Soul Monk who seeks to restore Sunrise Spire. We've been given a Sun Crystal to place at the pinnacle of the spire. We should find a way to reach it.`
  - стало: `We met a Sun Soul Monk, Mapo, who seeks to restore Sunrise Spire. He gave us a Sun Crystal meant to replace the one missing from here. He believes the way to the spire is accessed through the Sunrise Spire Vaults.`
  - текущий перевод: `Мы встретили монаха Солнечной души, который хочет восстановить Шпиль Рассвета. Нам дали солнечный кристалл, чтобы установить его на вершине шпиля. Надо найти путь наверх.`
- `hf4814ce4g7244g3686g5c8agedb23a2b8367` v24 -> v40
  - было:  `You have done a great service for me and my Order. Thank you. I want you to have this. It belonged to one of my old companions.`
  - стало: `I could feel the familiar warmth of the Morninglory even from here. You have done a great service to me and my Order. I want you to take this. It belonged to one of my old companions.`
  - текущий перевод: `Это огромная услуга мне и моему ордену. Спасибо. Хочу, чтобы это было у тебя. Вещь принадлежала одному из моих прежних спутников.`
- `hbd4e9752g5a64gcdd3g9886g40a3ac1b1805` v12 -> v28
  - было:  `Very well. Take this sun crystal to the spire pinnacle. Come find me again when you've restored the spire. Lathander guide your way!`
  - стало: `The doors at the end of the hall are locked but I suspect that might be the way into the Spire itself where the crystal must be taken. A key might be in the library, but I've heard strange noises coming from there, so watch yourself!`
  - текущий перевод: `Хорошо. Отнеси этот солнечный кристалл на вершину шпиля. Возвращайся ко мне, когда шпиль будет восстановлен. Пусть Латандер направляет твой путь!`

## Новые строки (первые 50)

- `h979c0947g96bcgd058gc78ege90b66a5571c` — Mushroom Circle
- `h21d64225ge677g9916g106dgf2a812c81af7` — Come find me again when you've restored the spire. Lathander guide your way!
- `hd39cf8cag9258gb7feg0a00g7c698d091dac` — I, too, would see this holy site restored to glory one day. How can we help?
- `h0164201eg6070g5b01gc784g6b29d72ae83d` — I would be honoured to help a fellow Monk on their path. How can we help?
- `h90735d59gac38gc77bg224cgad55ed52546a` — I appreciate the offer stranger, but this holy quest must be mine alone.
- `hc6857b7fga3b7gcefag8766ge6d2b3f7e257` — I, too, would see this holy site restored to glory one day. How can we help?
- `h70d239fdg8d3cg035bg4b33gf9d15712c700` — Rosethorn Needler
- `he17014b9g470bg449ag936fg2801af9f9d71` — Wild Magic Wisp
- `h6ea8b361g4c78g0e9cg99f8g42043ad9d656` — Wild Magic Wisp
- `h36140cb5gdf2cg2905g663bg25bf000954de` — Wild Magic Wisp
- `ha55e371eg78e0g3ff4g75f1g90e13daa4250` — Rosethorn Crusher
- `h3eb8d633ga3bfga632gfd4cg1b8adfaca5d6` — Rosethorn Crusher
- `hd5157af9gedb6g823bg2eadg6c5dfd95bfad` — Wild Magic Wisp
- `he86006dag48d0g0ce8gbe4cg37e52aca3803` — Blink Dog
- `h366909cagbd6ag38dcgdf13g46facf19411c` — Blink Dog
- `h2dda666fg3ccdg753fgf2e2gf281ced7eb33` — Blink Dog
- `h83cb2fe8gbd81g0d90g65b5g7a2720a4210b` — Blink Dog
- `h7c49fb09g0459g4a6dg2198gf045c3f062be` — Blink Dog
- `h0bc20a1fgf101g08cega00age338936733f6` — Blink Dog
- `h8d2bd709gf530gae78gdd89g81774ffa04be` — Blink Dog
- `hcd02b872gea90gb6f9ga99bgced468541656` — Blink Dog
- `haab8d083gddcegbbb1gfbf2g96ec0a6eb91c` — Blink Dog
- `h52924997gb500ge9a7g69e4gd279a91ff744` — Blink Dog
- `hce7e0497g106cg9221g8275gce2bbfd49654` — Blink Dog
- `h2d951b03gb062g677bgff89ge1b5d1b989eb` — Blink Dog
- `hab70ed2eg94a7gcbd4g1da0g860145aaae81` — Blink Dog
- `he063c2c3g5171gba66ga390g232ed84e9f36` — Rosethorn Crusher
- `h9d26deacg9a8cg2c91ga6a4g5a0a0857b45b` — Rosethorn Vine
- `h563530ecgf281g57abgcf06gde88a6bab8a9` — Wild Magic Wisp
- `h2ffaad97gebecg926ag2752g53da9e8fe1a5` — Giant Rosethorn Vine
- `h2a106898g501bg4550g6449gd508bbae8333` — Rosethorn Crusher
- `h42fa449bgd5b1g7140g3d92g74cbecc66826` — Rosethorn Vine
- `h1cb86c21gb6feg504fg4afeg041a406a6c28` — Rosethorn Crusher
- `h8b6aec26g6e97g012fg6636g1465b9334aaf` — Rosethorn Vine
- `h39ee2c86g88a4g7c43g37f6g794502e4eaff` — Rosethorn Vine
- `hec098d86gbb05g5ee8g216dg322c61b36dd7` — Rosethorn Vine
- `h884e7271gfc3fga4b1g5e5bgbfcaad6744f9` — Rosethorn Vine
- `h7727e3e2g62b9g27d1gf84agb51086510597` — Rosethorn Vine
- `h57c2eca0g2fe5gfd0cg5d40g699ab0c77224` — Wild Magic Wisp
- `hd4f03ab4gf472g7aecg8bc6g286f16bbeba4` — Wild Magic Wisp
- `he7f3f414g293cgd334gc958g27e2cd041112` — Wood Woad
- `hf40ed100gd4f0gc416ga64dg1277d5062923` — Wood Woad
- `h7f277a9eg30f0gbdf6g6b09gf467fdbf6511` — Wood Woad
- `h7ee080d3g4c26g7861gbaf8g0cc03fe9c40d` — Shadow Strikes
- `h3bc1f8bfg6825g548egb039g58c35f36cd1e` — While its wielder is hidden, this weapon deals an extra [1].
- `h9869c13egc553g6fb8g66b0g1bace793e56f` — Shadow Strikes
- `h0a35729bg5021g114bg5020g7bdf0bd3d452` — Deal an additional [1] while <LSTag Type="Status" Tooltip="HIDDEN">Hidden</LSTag>.
- `h6ef297bfgbb5fg4a26gc68ag9df2b827b29b` — Shadar-Kai Spear
- `hbc887822g28c4g0820g3531g664908fe0d99` — The tip of this spear strikes unerringly towards its target's eyes.
- `h3ed98639gb961g8f03g0ff0g54bdf9a31ed7` — Blink Dog

…и еще 49.
