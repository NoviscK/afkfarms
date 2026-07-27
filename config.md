---
title: Configuração
permalink: /config/
---

**[🏠 Início](/) · [📋 Farms](/farms/) · [🧪 Tanque de XP](/tanque-xp/) · [🧴 Frasco de Alma](/frasco-alma/) · [⚙️ Config](/config/) · [📜 Changelog](/changelog/) — [🇬🇧 English](/en/config/)**

# Configuração (`config.json`)

Todas as farms, combustíveis e regras globais do mod são controladas por um único arquivo, gerado automaticamente na primeira vez que o mod carrega:

```
config/nvkmods/config.json
```

Edite esse arquivo e reinicie o mundo/servidor para aplicar as mudanças. Nenhum programa adicional é necessário — é só um arquivo de texto.

## Configurações globais

```json
"global_settings": {
  "xp_tank_max_level": 30,
  "allow_mending_repair": true,
  "allow_bottle_fill": true,
  "consume_input_item": true,
  "input_item_durability_uses": 64
}
```

| Campo | O que faz |
|---|---|
| `xp_tank_max_level` | Nível máximo que o [Tanque de XP](/tanque-xp/) guarda. |
| `allow_mending_repair` | Liga/desliga o reparo instantâneo com Remendo no Tanque de XP. |
| `allow_bottle_fill` | Liga/desliga a criação de Frasco de Experiência no Tanque de XP. |
| `consume_input_item` | Se `false`, o item de ativação nunca se gasta (dura pra sempre, como era antes). |
| `input_item_durability_uses` | Quantos ciclos de produção cada item de ativação aguenta por padrão. |

## Combustíveis

```json
{ "fuel_id": "minecraft:coal", "burn_time_seconds": 300, "drop_interval_seconds": 60 }
```

Cada combustível define quanto tempo dura (`burn_time_seconds`) e a velocidade de produção enquanto ativo (`drop_interval_seconds`).

## Farms

Cada farm no array `farms` define: `farm_id`, `input_item` (ou `requires_soul_jar: true`), `xp_per_drop`, `allowed_fuels`, `entity_type` (mob exibido no terrário), `scale`/`y_offset` (ajuste visual), `hostile`, `held_item`, `max_uses` (sobrescreve o padrão global) e `drops` (lista de `item_id`, `chance_percent`, `min_count`, `max_count`), além de `farm_block` (`afk_farm` ou `afk_nether_farm`).

Quer adicionar uma farm nova? Copie um bloco existente no array, mude os valores, e reinicie — sem precisar editar nenhum código.
