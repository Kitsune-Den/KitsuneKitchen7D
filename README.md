# KitsuneKitchen7D

🦊 **Part of the [Kitsune Systems Collection](https://github.com/Kitsune-Den)** —
[KitsunePvPExtended](https://github.com/Kitsune-Den/KitsunePvPExtended) ·
[KitsuneTrapXP](https://github.com/Kitsune-Den/KitsuneTrapXP) ·
[KitsuneZombieReach](https://github.com/Kitsune-Den/KitsuneZombieReach) ·
[KitsuneFuelSaver](https://github.com/Kitsune-Den/KitsuneFuelSaver) ·
[KitsuneFoxacary](https://github.com/Kitsune-Den/KitsuneFoxacary)

[![Download on Nexus Mods](https://img.shields.io/badge/Download-Nexus_Mods-da8e35?style=flat&logo=nexusmods&logoColor=white)](https://www.nexusmods.com/7daystodie/mods/10022)
[![7 Days to Die v3.3](https://img.shields.io/badge/7_Days_to_Die-v3.3-8b0000?style=flat)](https://7daystodie.com)
[![License](https://img.shields.io/badge/license-CC_BY--NC--SA_4.0-blue?style=flat)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/Kitsune-Den/KitsuneKitchen7D?style=flat&logo=github)](https://github.com/Kitsune-Den/KitsuneKitchen7D/stargazers)

A fox-crafted cooking expansion for **7 Days to Die**. Adds 22 new food and drink items with custom buffs, all craftable from the start and none of them smelly to zombies, and a long-overdue Sham Sandwich vendor fix.

The philosophy is simple: take what the wasteland already gives you and make something greater from it. Simple dishes from raw ingredients, elevated meals from already-cooked foods, and drinks that'd make a pre-apocalypse barista jealous.

## Installation

1. Download or clone this repository
2. Copy the `KitsuneKitchen7D` folder into your 7 Days to Die `Mods/` directory
   - **Client:** `%APPDATA%/7DaysToDie/Mods/` or `<SteamDir>/steamapps/common/7 Days to Die/Mods/`
   - **Dedicated Server:** `<ServerDir>/Mods/`
3. Restart the game or server
4. Confirm the mod loads in the **Mods** menu

No additional dependencies required. Works alongside other modlets.

## Compatibility

- **7 Days to Die v3.0 – v3.3** (verified against v3.3 b18 game data)
- Server-side and client-side compatible
- EAC: Must be **disabled** (as with all modlets)
- **13 languages:** English, German, Spanish, French, Italian, Japanese, Korean, Polish, Brazilian Portuguese, Russian, Turkish, Simplified Chinese, Traditional Chinese

## What's Included

### Vanilla Fix

| Fix | Details |
|-----|---------|
| Sham Sandwich Sellable | Flips `SellableToTrader` to true and sets `EconomicValue` so traders will actually buy them (~2.5 dukes each) |

### Zero-Smell Cooking

Every Kitsune dish and drink has **zero smell**: eating one won't draw zombies, unlike most of the vanilla meals they're made from. The one deliberate exception is the Walker Milkshake (see below).

### Simple Dishes

Early-game recipes from raw ingredients. Crafted at the **campfire with grill or cooking pot**.

| Dish | Ingredients | Station | Food | Health | Water | Stamina | Buff |
|------|------------|---------|------|--------|-------|---------|------|
| Fox's Hash | Potato + Egg | Grill | 22 | 8 | — | +10 | — |
| Mushroom Omelette | 2x Mushrooms + Egg | Grill | 20 | 8 | — | +10 | — |
| Honey Corn Cake | Corn + Honey | Grill | 18 | 5 | 5 | +10 | 5% infection cure |
| Burnt Ends | 2x Charred Meat + 4x Raw Meat | Grill | 35 | 15 | — | +10 | — |
| Forager's Broth | 2x Mushrooms + Corn + Boiled Water | Pot | 25 | 10 | 15 | +10 | — |
| Harvest Pumpkin Soup 🎃 | 2x Pumpkin + Corn + Boiled Water | Pot | 30 | 14 | 15 | +10 | — |
| Kitsune Udon 🦊 | Canned Miso + 2x Corn Meal + Egg + Animal Fat + Boiled Water | Pot | 45 | 22 | 20 | +20 | Fox's Favor |
| Country Fried Steak | Sham Sandwich + 2x Egg + 2x Grilled Meat | Pot | 60 | 22 | 5 | +20 | Hearty |

### Drinks

Smoothies are crafted **in your backpack** (like Yucca Smoothie, and sped up by Pack Mule). Teas and lattes are crafted at the **campfire with cooking pot**. Every drink puts you out if you're on fire.

| Drink | Ingredients | Station | Health | Water | Buff |
|-------|------------|---------|--------|-------|------|
| Blueberry Smoothie | 3x Blueberries + Boiled Water | Backpack | 5 | 25 | — |
| Aloe Cooler | 2x Aloe Leaf + Blueberries + Boiled Water | Backpack | 8 | 30 | Refreshed |
| Espresso Smoothie | Coffee + Snowball | Backpack | 5 | 20 | Wired |
| Herbal Honey Tea | Honey + Aloe Leaf + Yucca Fibers + Boiled Water | Pot | 10 | 30 | Herbal Remedy (15% infection + 20% dysentery cure) |
| Pumpkin Spice Latte 🎃 | Coffee + Pumpkin + Honey | Pot | 5 | 30 | Cozy |

Herbal Honey Tea replaces the vanilla Honey Tea recipe, so it's the only craftable honey tea. Vanilla Honey Tea still shows up in loot and at traders.

### Completed Works

Elevated meals crafted from **already-cooked dishes**. You're not just cooking — you're composing a meal from meals. Each one is worth more than its ingredients eaten separately, *plus* a buff. All crafted at the **campfire with cooking pot**.

| Dish | Ingredients | Makes | Food | Health | Water | Stamina | Buff |
|------|------------|-------|------|--------|-------|---------|------|
| Fox's Breakfast | Bacon & Eggs + Corn Bread | 1 | 55 | 28 | 5 | +25 | — |
| Wasteland Chowder | Sham Chowder + Corn on the Cob | 1 | 70 | 90 | 15 | +40 | Sham Chowder (+1 Fortitude) |
| Hot Honey Chicken 🐔 | Chicken Nuggets + Corn Bread + Honey | 1 | 55 | 26 | — | +25 | Hearty, 5% infection cure |
| Hunter's Bounty | Meat Stew + Baked Potato + Boiled Egg | 1 | 80 | 40 | 20 | +40 | Hearty |
| Scavenger's Stir Fry | Veggie Stew + Grilled Meat + Corn Bread | 1 | 60 | 30 | 20 | +40 | Energized |
| Harvest Pot Pie 🎃🐔 | Ash Chicken Stew + Pumpkin Bread | 1 | 100 | 50 | 20 | +40 | Hearty |
| Kitsune Gumbo | Gumbo Stew + Fish Tacos + Corn on the Cob | **2** | 90 | 52 | 10 | +40 | Spicy |
| Survivor's Feast | Steak & Potato + Spaghetti + Blueberry Pie | **2** | 115 | 56 | 10 | +40 | Well Fed |

Stats for Gumbo and Feast are per serving.

### Cursed Secret Menu

| Drink | Ingredients | Station | Effect |
|-------|------------|---------|--------|
| Walker Milkshake | 3x Rotting Flesh + Blood Bag + River Water | Workbench | Max smell for 60 seconds. Every walker within 100m comes to find you. Horde bait. |

### Custom Buffs

| Buff | Duration | Effects |
|------|----------|---------|
| Refreshed | 5 min | Light health + stamina regen |
| Wired | 10 min | +15% run speed, stamina regen |
| Herbal Remedy | 5 min | Health regen (alongside the tea's infection + dysentery cure) |
| Cozy | 20 min | Stamina regen, +15 cold resistance |
| Fox's Favor | 20 min | +10% loot stage, 15% faster looting |
| Hearty | 15 min | Health regen, +10% physical damage resistance |
| Energized | 15 min | Stamina regen, +10% run speed |
| Spicy | 30 min | Stamina regen, +15% physical damage resistance |
| Well Fed | 45 min | Health + stamina regen, +15% damage resistance, +10% block damage |

### Plays Nice With Vanilla Systems

- **Quality cooking tools:** a higher-quality Cooking Grill or Cooking Pot crafts Kitsune recipes faster, same as vanilla food.
- **Farmer armor set:** the set's food bonus applies to Kitsune dishes.

### Recipe Unlocks

All recipes are **craftable from the start** — no magazines or skill gating. You just need the ingredients and the right crafting station.

> Earlier versions gated recipes behind **Home Cooking Weekly** magazines via the vanilla `craftingFood` skill. That broke on progression overhauls (e.g. *Learn By Doing*, which replaces the entire `/progression` tree and removes `craftingFood`, leaving the recipes permanently locked). Unlocking by default keeps Kitsune Kitchen compatible with vanilla **and** every overhaul.

## Mod Structure

```
KitsuneKitchen7D/
├── ModInfo.xml              # Mod metadata
├── Config/
│   ├── items.xml            # 22 new items + Sham Sandwich fix
│   ├── recipes.xml          # 22 crafting recipes
│   ├── buffs.xml            # 10 custom buffs
│   ├── progression.xml      # (no gating — recipes unlock by default)
│   └── Localization.csv     # Display names & descriptions
└── README.md
```

## Credits

- **AdaInTheLab** — Design, development
- **Maltaine** — Burnt Ends + Country Fried Steak recipe ideas, espresso smoothie QA tester extraordinaire
- **The Skulk** — KitsuneDen mod family

## License

[CC BY-NC-SA 4.0](LICENSE), with an extra permission for servers that make money: see [NOTICE.md](NOTICE.md). In short: play it, change it and share it, with credit, not for sale, and with changed versions under the same license.
