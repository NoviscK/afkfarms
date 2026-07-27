---
title: Configuration
permalink: /en/config/
---

**[🏠 Home](/en/) · [📋 Farms](/en/farms/) · [🧪 XP Tank](/en/xp-tank/) · [🧴 Soul Bottle](/en/soul-bottle/) · [⚙️ Config](/en/config/) · [📜 Changelog](/en/changelog/) — [🇧🇷 Português](/config/)**

# Configuration (`config.json`)

Every farm, fuel, and global rule in the mod is controlled by a single file, auto-generated the first time the mod loads:

```
config/nvkmods/config.json
```

Edit the file and restart the world/server to apply changes. No extra tools needed — it's just a text file.

## Global settings

```json
"global_settings": {
  "xp_tank_max_level": 30,
  "allow_mending_repair": true,
  "allow_bottle_fill": true,
  "consume_input_item": true,
  "input_item_durability_uses": 64
}
```

| Field | What it does |
|---|---|
| `xp_tank_max_level` | Max level the [XP Tank](/en/xp-tank/) stores. |
| `allow_mending_repair` | Toggles instant Mending repair on the XP Tank. |
| `allow_bottle_fill` | Toggles creating Bottles o' Enchanting from the XP Tank. |
| `consume_input_item` | If `false`, activation items never wear out (last forever, like before). |
| `input_item_durability_uses` | How many production cycles each activation item survives by default. |

## Fuels

```json
{ "fuel_id": "minecraft:coal", "burn_time_seconds": 300, "drop_interval_seconds": 60 }
```

Each fuel defines how long it lasts (`burn_time_seconds`) and the production speed while active (`drop_interval_seconds`).

## Farms

Each entry in the `farms` array defines: `farm_id`, `input_item` (or `requires_soul_jar: true`), `xp_per_drop`, `allowed_fuels`, `entity_type` (mob shown in the terrarium), `scale`/`y_offset` (visual tuning), `hostile`, `held_item`, `max_uses` (overrides the global default), and `drops` (a list of `item_id`, `chance_percent`, `min_count`, `max_count`), plus `farm_block` (`afk_farm` or `afk_nether_farm`).

Want to add a new farm? Copy an existing entry in the array, change the values, and restart — no code editing required.
