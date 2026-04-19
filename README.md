# KitsuneKitchen7D

[![Download on Nexus Mods](https://img.shields.io/badge/Download-Nexus_Mods-da8e35?style=flat&logo=nexusmods&logoColor=white)](https://www.nexusmods.com/7daystodie/mods/10022)
[![7 Days to Die v2.5](https://img.shields.io/badge/7_Days_to_Die-v2.5_Survival_Revival-8b0000?style=flat)](https://7daystodie.com)
[![License](https://img.shields.io/badge/license-CC_BY--NC_4.0-blue?style=flat)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/Kitsune-Den/KitsuneKitchen7D?style=flat&logo=github)](https://github.com/Kitsune-Den/KitsuneKitchen7D/stargazers)

A fox-crafted cooking expansion for **7 Days to Die**. Adds 16 new food and drink items with custom buffs, a magazine-gated progression system, and a long-overdue Sham Sandwich vendor fix.

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

- **7 Days to Die v2.5** (Survival Revival)
- Server-side and client-side compatible
- EAC: Must be **disabled** (as with all modlets)

## What's Included

### Vanilla Fix

| Fix | Details |
|-----|---------|
| Sham Sandwich Sellable | Flips `SellableToTrader` to true and sets `EconomicValue` so traders will actually buy them (~2.5 dukes each) |

### Simple Dishes

Early-game recipes from raw ingredients. Crafted at the **campfire with grill or cooking pot**.

| Dish | Ingredients | Station | Food | Health | Water | Stamina |
|------|------------|---------|------|--------|-------|---------|
| Fox's Hash | Potato + Egg | Grill | 22 | 8 | — | +10 |
| Mushroom Omelette | 2x Mushrooms + Egg | Grill | 20 | 8 | — | +10 |
| Honey Corn Cake | Corn + Honey | Grill | 18 | 5 | 5 | +10 |
| Burnt Ends | 2x Charred Meat + 4x Raw Meat | Grill | 28 | 12 | — | +10 |
| Forager's Broth | 2x Mushrooms + Corn + Boiled Water | Pot | 25 | 10 | 15 | +10 |

### Drinks

Smoothies and coolers crafted at the **workbench** (like Yucca Smoothie). Teas at the **campfire with cooking pot**.

| Drink | Ingredients | Station | Health | Water | Buff |
|-------|------------|---------|--------|-------|------|
| Blueberry Smoothie | 3x Blueberries + Boiled Water | Workbench | 5 | 25 | — |
| Aloe Cooler | 2x Aloe Leaf + Blueberries + Boiled Water | Workbench | 8 | 30 | Refreshed |
| Espresso Smoothie | Coffee + Snowball | Workbench | 5 | 20 | Wired |
| Herbal Honey Tea | Honey + Aloe Leaf + Yucca Fibers + Boiled Water | Pot | 10 | 20 | Herbal Remedy (15% infection cure) |

### Completed Works

Elevated meals crafted from **already-cooked dishes**. You're not just cooking — you're composing a meal from meals. All crafted at the **campfire with cooking pot**.

| Dish | Ingredients | Food | Health | Water | Stamina | Buff |
|------|------------|------|--------|-------|---------|------|
| Country Fried Steak | Sham Sandwich + 2x Egg + 2x Grilled Meat | 60 | 22 | 5 | +20 | Hearty |
| Fox's Breakfast | Bacon & Eggs + Corn Bread | 45 | 15 | 5 | +15 | — |
| Wasteland Chowder | Sham Chowder + Corn on the Cob | 40 | 10 | 10 | +15 | — |
| Hunter's Bounty | Meat Stew + Baked Potato + Boiled Egg | 55 | 20 | 5 | +20 | Hearty |
| Scavenger's Stir Fry | Veggie Stew + Grilled Meat + Corn Bread | 55 | 20 | 5 | +20 | Energized |
| Kitsune Gumbo | Gumbo Stew + Fish Tacos + Corn on the Cob | 65 | 25 | 10 | +30 | Spicy |
| Survivor's Feast | Steak & Potato + Spaghetti + Blueberry Pie | 80 | 30 | 10 | +40 | Well Fed |

### Custom Buffs

| Buff | Duration | Effects |
|------|----------|---------|
| Refreshed | 5 min | Light health + stamina regen |
| Wired | 10 min | +15% run speed, stamina regen |
| Herbal Remedy | 5 min | Health regen, 15% infection cure |
| Hearty | 15 min | Health regen, +10% physical damage resistance |
| Energized | 15 min | Stamina regen, +10% run speed |
| Spicy | 30 min | Stamina regen, +15% physical damage resistance |
| Well Fed | 45 min | Health + stamina regen, +15% damage resistance, +10% block damage |

### Magazine Progression

All recipes unlock through **Home Cooking Weekly** magazines via the `craftingFood` skill. They're woven into the existing vanilla tiers so they feel like a natural part of the game.

| Food Level | Unlocks |
|-----------|---------|
| 2 | Fox's Hash, Mushroom Omelette |
| 4 | Honey Corn Cake |
| 6 | Burnt Ends |
| 8 | Forager's Broth |
| 11 | Blueberry Smoothie |
| 14 | Aloe Cooler, Herbal Honey Tea |
| 22 | Espresso Smoothie |
| 27 | Fox's Breakfast, Wasteland Chowder |
| 35 | Country Fried Steak |
| 43 | Hunter's Bounty |
| 51 | Scavenger's Stir Fry |
| 80 | Kitsune Gumbo |
| 100 | Survivor's Feast |

## Mod Structure

```
KitsuneKitchen7D/
├── ModInfo.xml              # Mod metadata
├── Config/
│   ├── items.xml            # 16 new items + Sham Sandwich fix
│   ├── recipes.xml          # 16 crafting recipes
│   ├── buffs.xml            # 7 custom buffs
│   ├── progression.xml      # Magazine unlock tiers
│   └── Localization.txt     # Display names & descriptions
└── README.md
```

## Credits

- **AdaInTheLab** — Design, development
- **Maltaine** — Burnt Ends + Country Fried Steak recipe ideas, espresso smoothie QA tester extraordinaire
- **The Skulk** — KitsuneDen mod family

## License

CC BY-NC 4.0 — Free to use and modify for non-commercial purposes with attribution.
