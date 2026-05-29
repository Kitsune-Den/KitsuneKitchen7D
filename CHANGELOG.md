# Changelog

All notable changes to Kitsune Kitchen are documented here.

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
