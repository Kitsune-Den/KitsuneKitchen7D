# Changelog

All notable changes to Kitsune Kitchen are documented here.

## [1.5.1] — 2026-10-20

### Added
- **Translations for 12 more languages:** German, Spanish, French, Italian, Japanese, Korean, Polish, Brazilian Portuguese, Russian, Turkish, Simplified Chinese and Traditional Chinese. Every item name, description, buff name and buff description now has a translation. Vanilla dishes mentioned in descriptions use the game's own translated names (for example Sham is «Срам» in Russian and nięso in Polish), so they match what players see in their inventory.

## [1.5.0] — 2026-10-20

### Added — the Harvest Menu 🎃🐔
Five new recipes that use the chicken and pumpkin ingredients vanilla has added since 3.1:
- **🎃 Pumpkin Spice Latte** (pot): Coffee + Pumpkin + Honey. Grants the new **Cozy** buff (stamina regen + cold resistance, 20 min).
- **Harvest Pumpkin Soup** (pot, early game): 2 Pumpkin + Corn + Boiled Water.
- **🦊 Kitsune Udon** (pot): Canned Miso + 2 Corn Meal + Egg + Animal Fat + Boiled Water. The fox's own dish. Grants the new **Fox's Favor** buff (+10% loot stage, 15% faster looting, 20 min).
- **Hot Honey Chicken** (Completed Work, tier 1): Chicken Nuggets + Corn Bread + Honey. Grants Hearty and a 5% infection cure.
- **Harvest Pot Pie** (Completed Work, tier 2): Ash Chicken Stew + Pumpkin Bread. Grants Hearty.

### Changed — Completed Works rebalance
Vanilla food has been rebalanced heavily, which left most Completed Works worth *less* than the dishes they consume. They now return more than their inputs would if eaten separately, plus their buff:
- **Fox's Breakfast:** 45/15/5/15 → 55/28/5/25 (food / health / water / stamina).
- **Wasteland Chowder:** 40/10/10/15 → 70/90/15/40, and it now keeps vanilla's **Sham Chowder** Fortitude buff instead of dropping it.
- **Hunter's Bounty:** 55/20/5/20 → 80/40/20/40 + Hearty.
- **Scavenger's Stir Fry:** 55/20/5/20 → 60/30/20/40 + Energized.
- **Kitsune Gumbo** and **Survivor's Feast** now make **two servings** per craft (90/52/10/40 and 115/56/10/40 each). Their inputs add up to more than a full stomach, so a single serving wasted most of it.
- **Burnt Ends:** 28/12 → 35/15, in line with the ~14 raw meat it costs.
- **Herbal Honey Tea** now also cures **20% dysentery**, matching vanilla Honey Tea, whose recipe this mod removes.
- **Honey Corn Cake** keeps honey's 5% infection cure.
- Trade values are set close to the combined value of each recipe's ingredients, so selling to traders is neither a loss nor a profit.

### Fixed
- **Zero-smell food now actually works.** Since v1.3.0, `SmellUse="0"` was set on the item itself, but the game only reads `SmellUse` from the item's `Action0` (eat action) block, so every dish still gave off its vanilla parent's 10–50m of smell. The override has moved into `Action0`. The Walker Milkshake's item-level smell moved there too; its 60-second smell buff was already working.
- **Better Cooking Grills and Pots now speed up Kitsune recipes.** Recipes now carry the vanilla `grill` / `cookingPotFood` tags that quality-tier crafting-time bonuses look for. Backpack smoothies are now tagged `packMuleCrafting` for the Pack Mule perk, and the Walker Milkshake is tagged `workbenchCrafting`.
- **The Farmer armor set bonus now boosts Kitsune food.** Every dish sets the `foodHealthFarmer` / `foodStaminaFarmer` values the set bonus multiplies.
- **Drinks put out fire again.** All Kitsune drinks now apply vanilla's `buffExtinguishFire` when you drink one while burning.
- **Country Fried Steak no longer gives a free jar.** It extended Meat Stew, which refunds an empty jar when eaten, even though the recipe uses no jar. It now extends Steak & Potato, which is served on a plate.

### Compatibility
- Verified against **7 Days to Die v3.3 (b18)** game data: every referenced item, buff, recipe tag, display type, passive effect and the `drinkJarHoneyTea` remove target exist. Tested in-game.

## [1.4.0] — 2026-06-15

### Changed
- **Updated for 7 Days to Die v3.0 "Dead Hot Summer."** v3.0 renamed the localization file from `Localization.txt` to `Localization.csv` (the old extension is no longer loaded), so the mod's localization file is renamed to match. The file's contents were already in CSV format, so no display names or descriptions changed.

### Compatibility
- Verified every vanilla dependency against the v3.0 game data: all 33 referenced items, both crafting stations (`toolCookingGrill`/`toolCookingPot`), the `perkMasterChef` tag, the removed `drinkJarHoneyTea` recipe, the `buffProcessConsumables`/`buffInfectionAddCure` buffs, the food/water/stamina CVars, the `smell` cvar, the Sham Sandwich trader properties, and all buff icons still exist unchanged. No recipe, item, or buff logic needed updating.

## [1.3.0] — 2026-05-29

### Added
- **🥤 Walker Milkshake** — a cursed secret-menu drink crafted at the **workbench** (rotting flesh + blood bag + jar of water). Chugging it maxes your scent and **re-pins it for 60 seconds**, drawing every walker within 100m to investigate your spot. Deliberate horde bait — kite to traps, clear a street, "hold my milkshake." Craft more if you want a longer party.

### Changed
- **Food no longer attracts zombies.** All 16 dishes now set `SmellUse="0"` — they were inheriting 10–50m of scent from their vanilla parents, so eating a Kitsune meal could quietly draw a crowd. Cooking should mask the smell; now it does.
- **The two honey teas are now one.** Buffed **Herbal Honey Tea** to be the definitive honey tea (+30 water, +12 food, +10 heal, keeps the Herbal Remedy regen + 15% infection cure) and removed the vanilla `drinkJarHoneyTea` *recipe* so it's the only craftable honey tea. (Vanilla item still drops in loot/traders, just not craftable.)

## [1.2.1] — 2026-05-29

### Fixed
- **Server error on progression overhauls (e.g. Learn By Doing).** 1.2.0 removed the recipe gating but the 16 food/drink *items* still carried `UnlockedBy="craftingFood"`. On a server where an overhaul deletes the vanilla `craftingFood` skill, each item referenced a progression that no longer exists and errored on load. Removed `UnlockedBy="craftingFood"` from all 16 items — recipes are already default-unlocked, so it was redundant, and dropping it lets each item inherit its vanilla parent's (overhaul-remapped) unlock.

## [1.2.0] — 2026-05-29

### Changed
- **Recipes now unlock by default** — removed the `learnable` tag from all 15 recipes, so they're craftable from the start with no magazine or skill gating.

### Fixed
- **Compatibility with progression overhauls** (e.g. *Learn By Doing*). Recipes were gated behind the vanilla `craftingFood` skill via `progression.xml`. Overhauls that replace the entire `/progression` tree (`<set xpath="/progression">`) delete `craftingFood`, which left the unlock `<append>` with no target — so the recipes never unlocked. Default-unlock removes that dependency entirely; Kitsune Kitchen now works on vanilla and every overhaul.
- Corrected `ModInfo.xml` version, which was still `1.0.0` despite the 1.1.0 release.

## [1.1.0] — 2026-03-31

### Added
- Country Fried Steak recipe.

### Fixed
- Sham Sandwich vendor fix (sellable to traders).
- Item descriptions and the Herbal Honey Tea infection-cure buff.

## [1.0.0] — 2026-03-30

### Added
- Initial release: 15 food/drink items, 7 custom buffs, and magazine-gated progression.
