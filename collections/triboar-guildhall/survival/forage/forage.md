# Forage (Survival Subalias)

Forage for edible plants and food in different environments.

## Usage

```
!survival forage <terrain> [options]
!survival forage help
```

## Terrains

- **grasslands** - Forage in open plains for grains, berries, and roots
- **forest** - Forage in wooded areas for mushrooms, nuts, and herbs
- **mountains** - Forage in mountainous regions for moss, lichen, and hardy plants

Servers may configure additional custom foraging terrains.

## How It Works

Foraging is a two-step process:

1. **Find Food** (Survival check) - Locate edible plants and resources
2. **Harvest** (Survival check) - Safely gather and prepare the food

## Options

- **-adv/-dis** - Roll with advantage/disadvantage
- **-fadv/-fdis** - Advantage/disadvantage on finding food
- **-hadv/-hdis** - Advantage/disadvantage on harvesting
- **-b [bonus]** - Add bonus to all rolls
- **-fb/-hb [bonus]** - Add bonus to specific rolls
- **-guidance** - Add 1d4 guidance to find/harvest rolls

## Features

- Different plant species per terrain
- Weight and safety DC vary by plant type
- Automatic harvesting by default
- Background features may provide bonuses (Wanderer)
- Results added to inventory

## Examples

```
!survival forage grasslands
!survival forage forest -adv
!survival forage mountains -guidance -fb 2
```

## Server Configuration

Servers can customize foraging with these svars:
- `ForageSpeciesGrasslands` - Grasslands plant data
- `ForageSpeciesMountains` - Mountains plant data
- `ForageSpeciesForest` - Forest plant data
- `HuntArgs` - Custom foraging terrain mappings (shared with hunt)
- `SurvSettings` - DC thresholds and harvest settings
