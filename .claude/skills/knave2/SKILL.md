---
name: knave2
description: Knave Second Edition (Ben Milton, 2024) rules reference for this Owlbear extension — abilities, checks, item slots and wounds, combat, spellcasting, leveling, equipment, monsters, plus every d100 table. Load when modelling or implementing any Knave concept (character sheet fields, HP and wound tracking, token stats, spells per day, armor class), when a rules question comes up, or when the user names a Knave mechanic (slots, wounds, careers, relics, hazard die, power attack, morale).
---

# Knave: Second Edition

Rules reference distilled from the full rulebook. Everything an implementation needs is either on this page or one pointer away in `reference/`. Book page numbers are cited as `(p. N)` throughout — the book's own tables cross-reference each other that way, and the [page map](#page-map) at the bottom resolves a page to a file.

Source: *Knave: Second Edition*, © 2024 Ben Milton and Questing Beast LLC. Game mechanics may be reused freely; the text and art may not. Anything published must carry: "[product name] is an independent production of [publisher name] and is not affiliated with Questing Beast LLC."

## The system in one paragraph

Classless old-school fantasy. A PC is six ability scores (0–10, starting 0–3), a level (1–10) with XP, HP (level d6), two careers, and `10 + CON` item slots that double as the wound track. Every roll is the same **check**: `d20 + ability + modifiers ≥ 11 + difficulty`, difficulty defaulting to 5, so the typical target is 16. Modifiers come only in ±5 steps. Armor Class is `11 + armor points` and is just a check's target number. There are no classes, no skills, no saving throws, no spell levels, no coin denominations — a PC's niche is which abilities they raise and what fills their slots.

## Ability scores (p. 4)

Six abilities, scores 0–10, each linked to an archetype and to a hard mechanical resource:

| # | Ability | Archetype | Added to | Resource it governs |
| --- | --- | --- | --- | --- |
| 1 | **STR** Strength | Fighter | Melee attacks; power checks (climbing, lifting, breaking free) | — |
| 2 | **DEX** Dexterity | Thief | Agility and reflexes (dodging, sneaking, pickpocketing, sleight of hand) | — |
| 3 | **CON** Constitution | Adventurer | Resisting poison, cold, fatigue, drowning, etc. | `10 + CON` item slots = `10 + CON` wounds before death |
| 4 | **INT** Intelligence | Magic-User | Cunning (lockpicking, alchemy) | Spellbooks usable per day = INT; spell effect magnitude = INT |
| 5 | **WIS** Wisdom | Ranger | Ranged attacks; perception and willpower (foraging, navigation, resisting spells, surprise) | — |
| 6 | **CHA** Charisma | Cleric | Force of personality (initiative, persuasion, morale rerolls) | Max companions = CHA; max active blessings = CHA |

The numbering matters: the random creation method maps a d6 result to the ability with that number.

## Checks (p. 7)

`d20 + ability score + modifiers`. Success if the total **meets or exceeds** the target number.

- **Target number** = `11 + difficulty`. Difficulty is 0–10, default **5** (so default target 16). Against a creature, difficulty = its relevant ability score or level. In an attack, difficulty = the defender's armor points, and `11 + AP` is called **Armor Class**.
- **Creatures without ability scores** (monsters, NPCs) use their level, half their level, or 0, at the GM's judgement of how good they are at the task.
- **Modifiers** are only ever **+5 per advantage** and **−5 per disadvantage** (related career, clever approach, extra time, right tools, positioning, cover, visibility…). Careers add +5 to related *non-combat* checks only — never to attacks or maneuvers.
- **Reversible**: because a score becomes a target number by adding 11, either side can roll without changing the odds. A goblin (level 1) attacking a PC with 3 AP either rolls `d20 + 1` vs 14, or the PC rolls `d20 + 3` vs 12.
- **No lore checks**: PCs know all common knowledge and everything covered by their careers; other knowledge is found in play.
- **No search checks**: hidden things are found by spending time (one 10-minute turn per dungeon room, one 4-hour watch per wilderness hex) or by interacting with the world.
- **Social checks**: PC's CHA vs the NPC's WIS or CHA, only when the outcome is genuinely risky; disposition, bribes, threats, and phrasing are ±5 modifiers.
- **Saving-throw conversion** (p. 74) for imported material, usually vs target 16: STR resists restraint (hold, paralysis); DEX resists things that can be dodged (breath, blasts, rays, wands); CON resists body-altering effects (poison, death, petrification, polymorph); INT resists magical devices; WIS resists mind effects (spells, illusions).

## PC creation (p. 4)

1. **Ability scores.** Distribute **3 points** among the six scores (stacking allowed), or roll **3d6** and add 1 to the ability whose number each die shows (roll 3-5-5 → CON 1, WIS 2, rest 0). Starting scores are therefore 0–3.
2. **Secondary stats.** Level 1, 0 XP, `10 + CON` item slots, max HP = **1d6**.
3. **Careers.** Roll or pick **two** careers from the d100 list (→ `reference/careers.md`). Gain both careers' three items, plus whatever of the following fits in the slots: `3d6 × 10` coins, 2 rations, a 50′ rope, 2 torches, **any** armor pieces and weapons from the equipment list (p. 38), and a quiver of 20 arrows. A PC with INT ≥ 1 may receive one random spellbook **per point of INT**.
4. **Armor.** AP = number of armor pieces worn (max 7). AC = `AP + 11` (max 18).
5. **Name and description** — tables on pp. 54–59 (→ `reference/society.md`).

### Character sheet fields (p. 75)

The official sheet has exactly: Name · Careers · AC · AP · Level · XP · Max HP · HP · Portrait · the six abilities (each with a one-line reminder of what it covers) · **20 numbered item slots** in two columns of ten. There is no separate wound track — wounds are written *into* the slots. A sheet has 20 slots printed because `10 + CON` caps at 20 when CON is 10.

## Item slots and wounds (p. 6)

- **Slots** = `10 + CON`. Most items take **1 slot**, including a handful of small things that fit in one hand (10 candles, 20 arrows in a quiver, 10 rat traps). **Two-handed** items take **2 slots**. **500 coins** fill one slot. Armor pieces take 1 slot each and are worn, not carried separately. Spellbooks and relics take at least 1 slot.
- **Damage** reduces HP. Once HP is **0**, each further point of damage fills one slot with a **wound** (stabbed, frozen, burned…), starting from the **highest-numbered** slot and working down. Anything in a wounded slot must be **dropped**.
- **Direct damage** bypasses HP and goes straight to wounds. It applies whenever combat skill would not protect the creature: falls, sneak attacks, attacks on the unaware, environmental hazards, exceeding travel limits, and hits against a weakness. Creatures **without slots** (monsters) take **triple** damage from direct damage instead.
- **Death.** A PC dies when **every** slot is wounded — i.e. after `10 + CON` wounds past 0 HP. Monsters and NPCs simply die at 0 HP.
- **Healing.** HP returns to **maximum every morning** after two watches (8 hours) of sleep and a meal the previous night. In a **safe haven** this also heals **one wound** per night. The book does not define "safe haven" beyond noting that a magically conjured house (*manse*) does not count; read it as a settlement or comparable secure shelter. Wounds therefore heal one per day and only in town. Rare-item salves, potions of healing, and blessings are the only faster routes.
- The designer notes GMs may rule certain wounds heal slower or need treatment, and may optionally rule that the item in a wounded slot breaks ("hard mode").

## Leveling up (p. 6)

- **XP = coins.** 1 XP per coin of treasure value recovered from a remote dangerous place **and returned to civilization**, split evenly among the PCs who took part. Imported adventures: convert everything to gold pieces and grant that many XP. Carousing (p. 52) also grants XP equal to coins spent.
- XP is **never reset**; the thresholds are cumulative totals.
- **On gaining a level:** add **+1 to three different ability scores** (player's choice or random; max 10 each), and **reroll max HP** with the new number of d6 — if the new total is not higher than the old maximum, use `old max + 1` instead.

| Level | XP total | Max HP roll | Title |
| --- | --- | --- | --- |
| 1 | 0 | 1d6 | Wretch |
| 2 | 2,000 | 2d6 | Lowlife |
| 3 | 4,000 | 3d6 | Hoodlum |
| 4 | 8,000 | 4d6 | Fool |
| 5 | 16,000 | 5d6 | Dastard |
| 6 | 32,000 | 6d6 | Cad |
| 7 | 64,000 | 7d6 | Gadabout |
| 8 | 125,000 | 8d6 | Rogue |
| 9 | 250,000 | 9d6 | Jack |
| 10 | 500,000 | 10d6 | Knave |

The table ends at level 10 and ability scores cap at 10. With 3 points to start and 3 per level, a level-10 PC has 30 ability points total.

## Combat (p. 20)

- **Rounds** are 10 seconds. **Initiative**: one CHA vs CHA check between the two sides' leaders; the winning side acts first as a group. On its turn each creature may **move** (40′ for PCs) and take **one other action** (attack, cast, move again, maneuver…).
- **Attack** = a check: **STR** for melee, **WIS** for ranged, vs the defender's **AC** (`11 + AP`). A hit deals the weapon's damage die.
- **Natural 1**: the weapon **breaks**. **Total ≥ 21**: hit, and the attacker may also succeed at a **free maneuver** of their choice.
- **Maneuvers** (disarm, push, trip, stun, blind, break gear, restrain, pickpocket, climb…) are resolved as an appropriate ability check, cause damage only indirectly (e.g. off a ledge), and are the intended way to bring down tough enemies.
- **Ranged**: cannot be made while the attacker is in melee; **−5** if the target is in melee.
- **Sneak attack**: a melee attack on an unsuspecting foe **always hits** and deals **direct damage**. A truly defenseless foe is simply killed.
- **Power attack**: after a *successful* melee attack roll, before damage, the PC may **double the damage dice** — and the weapon **breaks**.
- **Damage types**: against a **weakness**, damage becomes **direct**; against an **immunity**, it is **zero**.
- **Modifiers** (±5): positioning, ganging up, weapon type, aiming, visibility, cover, size, range, surprise, elevation. Careers never modify combat checks.
- **Morale**: at a **breaking point** NPCs roll **2d6 ≤ morale** or rout/surrender. Breaking points: losing half HP (if alone), the first casualty, half the force lost, the leader killed, being attacked by something they fear. Once per battle the side's leader may pass a CHA check to reroll a failed test. Morale runs 2–12, 7 average. PCs and companions never test morale.
- **Surprise** (p. 19) grants the surprising side the first turn and **+5 on all combat checks in round 1**.

## Environmental hazards (p. 21)

| Hazard | Effect |
| --- | --- |
| Fire | 1d6 direct/round; **on fire** 2d6 direct/round; immersed in lava = death |
| Drowning | Hold breath 30 s + 30 s per CON point; then pass a CON check every round or die |
| Freezing | 1 direct per 10-minute turn unless a CON check is passed |
| Lightning | 3d6 direct |
| Falling | 1d6 direct per 10′; if **three or more dice show 6**, instant death |
| Thirst | −5 to all checks per day without water; after 3 days, CON check daily or die |
| Sleep deprivation | −5 per day without sleep; after 2 days, WIS check every watch or pass out for 3 watches |
| Intoxication | CON check per hour of drinking; fail = drunk, −5 until next day; two consecutive fails = pass out for 2 watches |

## Spellcasting (p. 21)

- A **spellbook** holds **one spell**, takes **1 slot**, can be used **once per day**, and cannot be made or copied by PCs — only found or stolen.
- A PC can use **INT spellbooks per day**. INT 0 = no casting. Casting is one action.
- Wherever a spell text says **INT**, the caster substitutes **any number up to their INT**. That number is the spell's **level** when one is needed.
- Defaults: ongoing effects last **10 minutes (1 turn)**, range **40′**. An *item* is liftable in one hand; an *object* is anything up to human size.
- **Saves**: a targeted unwilling creature whose **level exceeds the spell's level** may check vs the spell's level (target `11 + level`). Success **halves** the effect; success by **10+ nullifies** it. Willing or lower-level targets get no save.
- **Chaos spellbooks** swap their spell for a random new one at the first dawn after casting.
- All 100 spells are utility spells, non-damaging at least directly. Rule of thumb for a generated damage spell: **INT × d6**.
- **Classic spellbooks** from other games (p. 73): a leveled spell needs caster **INT ≥ spell level**, is presented as a whole book, once per day, counts toward the INT limit. **Scrolls** can be cast by anyone, don't count toward the limit, and cannot be transcribed.
- Full spell list, generation tables → `reference/spells.md`.

## Relic magic (p. 32)

Cleric-type play. A **relic** is an item bound to a **patron** (petty god, saint, spirit, outsider). Owning a relic and having the patron's favor lets a PC speak to the patron at any of its **shrines**; the patron gives a **mission**, and on completion imbues the relic with an ongoing **blessing** (a minor aura or a small spell castable several times a day, designed jointly with the player). A PC may own any number of relics but have only **CHA active blessings**, reassigned each morning. Acting against the patron's goals brings **disfavor** and cuts the blessing off. → `reference/relics-alchemy.md`

## Equipment essentials (p. 38)

Currency is a single **coin (c)**; 10c is a day of unskilled labor. Rarity tiers: common 5c (any settlement), uncommon 20c (towns), rare 100c+ (cities).

| Item | Damage / effect | Slots | Cost |
| --- | --- | --- | --- |
| One-handed melee weapon | d6 | 1 | 50c |
| Two-handed melee weapon | d8 | 2 | 100c |
| Sling | d4, 60′ | 1 | 50c |
| Bow | d6, 120′, two hands | 2 | 100c |
| Quiver of 20 arrows | — | 1 | 5c |
| Armor piece (any of 7) | +1 AP each, max 7 AP | 1 each | see list |

Armor pieces: Shield 100c, Helmet 100c, Gambeson 100c, Mail shirt 200c, Breastplate 500c, Arm plate 500c, Leg plate 500c. Armor is tailored and has negligible resale value.

Prices, transport, animals, clothing, cost of living, all item tables → `reference/equipment.md`.

## Time and exploration (p. 8, p. 13)

Two clocks, each ended by a **hazard die** (d6: 1 encounter, 2 fatigue, 3 depletion/torch burn, 4 shift, 5 sign, 6 free):

- **Wilderness**: the day is six **4-hour watches** (3 day, 3 night). One 6-mile hex per watch, up to 3 per day; each extra watch of travel costs 1 direct damage unless a CON check is passed. Speed halves in darkness, rough terrain, or bad weather; doubles when riding.
- **Dungeon**: **10-minute turns**. Crawling 120′/turn (auto-detect traps, map), walking 2,400′ (surprised by everything, spring traps, can map), running 4,800′ (also cannot map; candles blow out). Torch: shapes 40′, detail 10′, burns out on a hazard-die 3. Candle: shapes 20′, detail 5′, lasts 8 hours, 10 per slot, searching takes 2 turns instead of 1. Total darkness: −10 to movement/coordination checks.

Full procedures, weather, encounters (distance, surprise, reaction, activity) and all location tables → `reference/exploration.md`.

## Monsters (p. 61)

A stat block is `AC, HP, LVL, ATK, MOV, MRL, NA`. HP ≈ `level × 4` or level d8. **Level** is the monster's default ability score for every check (half or 0 when it would be bad at the task). Monster AP = `AC − 11`. NA is number appearing (dungeon / wilderness). Default stand-in when improvising: the Owl bear (AC 14, HP 20, LVL 5). Bestiary and generator tables → `reference/monsters.md`.

## Downtime and hirelings (p. 52)

Carousing (d10 × 50/100/200c by settlement size, XP = coins spent, CON check or mishap), gambling, career training (1 month/1,000c common … 1 year/30,000c rare), hirelings 300c, mercenaries 600c, experts 600–2,400c, companions (PC-statted, half share, follow only higher-level PCs, lifetime max = CHA). → `reference/society.md`

## Implementation notes for the extension

Derived values, so store the inputs and compute the rest:

| Store | Derive |
| --- | --- |
| `str dex con int wis cha` (0–10) | slots `= 10 + con`; spells/day `= int`; blessings max `= cha`; companions max `= cha` |
| `level` (1–10), `xp` | title from the table; next threshold |
| `hpMax`, `hp` | hp is clamped `0..hpMax`; damage below 0 spills into wounds |
| `armorPieces` (0–7) | `ap = armorPieces`, `ac = 11 + ap` |
| `slots[1..10+con]` each `{ item?, wound? }` | wounds count = filled-with-wound slots; dead when all slots wounded; an item in a wounded slot is dropped |
| `careers[2+]` | +5 flag on related non-combat checks; never combat |

Damage algorithm: `hp -= dmg; if hp < 0 { overflow = -hp; hp = 0; wound the highest `overflow` unwounded slots, highest index first }`. Direct damage skips the HP step. Against a monster (no slots), direct damage is `dmg × 3` to HP.

Morning rest: `hp = hpMax`; if in a safe haven, clear one wound (the player picks which; the book does not specify an order).

Level up: `level += 1`; raise three *distinct* abilities by 1 (cap 10); `newMax = roll(level, d6); hpMax = newMax > hpMax ? newMax : hpMax + 1`.

## Reference files

| File | Contents |
| --- | --- |
| `reference/careers.md` | The d100 career table with starting items, and career-training rules |
| `reference/spells.md` | Spellcasting rules in full, the 100 spells, chaos books, spell generation (formulae, wizard names, qualities, effects, elements, forms), mutations, delusions, disasters, magic schools |
| `reference/relics-alchemy.md` | Patrons, relics, shrines, blessings, favor; domains and symbols; alchemy (brewing, harvesting), potions, textures, tastes, colors, ingredients |
| `reference/exploration.md` | Traveling, weather, delving, light, searching, encounters, hazard dice; travel shifts, signs, locations, structures, place traits, delve shifts, rooms, room details, room themes, dungeons, trap effects, hazards, mechanisms, activities |
| `reference/equipment.md` | Prices, transport, cost of living, coins vs. other games; tools, misc items, books, clothing, fabrics, decorations, treasures, materials, weapons, item traits |
| `reference/society.md` | Buildings and construction, warfare, downtime, recruiting; city themes, city events, street details, buildings, inn names, food; factions, missions, rewards, archetypes, names, surnames, personalities, NPC details, professions, goals, assets, liabilities, relationships, mannerisms |
| `reference/monsters.md` | Monster stats, the bestiary, monsters list; animals, organs, monster traits, powers, scents, sounds, tactics, weaknesses |
| `reference/gm-and-players.md` | GM duties, player duties, the gameplay example, designer's commentary |
| `reference/sample-maps.md` | The sample hex map (12 × 7 grid, named hexes) and sample dungeon map described, covers, illustration list |

## Page map

Resolves the book's `(p. N)` cross-references.

| Pages | Topic | File |
| --- | --- | --- |
| 1–3 | Introduction, GM duties, player duties | `gm-and-players.md` |
| 4 | Abilities, PC creation | this file |
| 5 | Careers | `careers.md` |
| 6–7 | Slots and wounds, leveling, checks | this file |
| 8–11 | Traveling, weather, travel shifts, signs, locations, structures, place traits | `exploration.md` |
| 13–17 | Delving, delve shifts, rooms, room details, room themes, dungeons, trap effects, hazards, mechanisms | `exploration.md` |
| 19 | Encounters, activities | `exploration.md` |
| 20–21 | Combat, hazards, spellcasting | this file |
| 22–25 | Spells | `spells.md` |
| 27–31 | Spell generation, wizard names, qualities, effects, elements, forms, mutations, delusions, disasters, magic schools | `spells.md` |
| 32–33 | Relic magic, domains, symbols | `relics-alchemy.md` |
| 35–37 | Alchemy, potions, textures, tastes, colors, ingredients | `relics-alchemy.md` |
| 38–43 | Equipment, tools, misc items, books, clothing, fabrics, decorations, treasures, materials, weapons, item traits | `equipment.md` |
| 44–51 | Buildings, warfare, city themes, city events, street details, buildings, inn names, food, factions, missions, rewards | `society.md` |
| 52–59 | Downtime, recruiting, archetypes, names, surnames, personalities, NPC details, professions, goals, assets, liabilities, relationships, mannerisms | `society.md` |
| 61–67 | Monsters, bestiary, animals, organs, monster traits, powers, scents, sounds, tactics, weaknesses | `monsters.md` |
| 68–74 | Gameplay example, designer's commentary | `gm-and-players.md` |
| 75 | Character sheet | this file (fields listed above) |
| 76–79 | Sample dungeon map, sample hex map | `sample-maps.md` |
| covers, 12, 18, 26, 34, 60, 70 | Cover art, back-cover blurb, full-page illustrations | `sample-maps.md` |
| 80–82 | Rules summary (duplicates pp. 4–53) | this file |
