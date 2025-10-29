# Hunt (Survival Subalias)

Hunt for game in various terrains to gather meat for food.

## Usage

```
!survival hunt <terrain> [options]
!survival hunt help
```

## Terrains

- **grasslands** - Hunt in open plains for game like deer and rabbits
- **forest** - Hunt in wooded areas for forest animals
- **mountains** - Hunt in mountainous regions for hardy mountain game

Servers may configure additional custom hunting terrains.

## How It Works

Hunting is a three-step process:

1. **Find Game** (Survival check) - Locate animals to hunt
2. **Kill the Animal** (Attack roll) - Make an accurate shot with your weapon
3. **Harvest** (Survival check) - Butcher and prepare the meat

## Options

- **-adv/-dis** - Roll with advantage/disadvantage
- **-fadv/-fdis** - Advantage/disadvantage on finding game
- **-kadv/-kdis** - Advantage/disadvantage on the kill shot
- **-hadv/-hdis** - Advantage/disadvantage on harvesting
- **-b [bonus]** - Add bonus to all rolls
- **-fb/-kb/-hb [bonus]** - Add bonus to specific rolls
- **-guidance** - Add 1d4 guidance to find/harvest rolls
- **-bless** - Add 1d4 bless to kill roll

## Features

- Different animal species per terrain
- Weight and AC vary by animal type
- Uses your best hunting weapon (bow, javelin, spear, trident, gun, yklwa)
- Automatic harvesting by default
- Background features may provide bonuses
- Results added to inventory

## Examples

```
!survival hunt grasslands
!survival hunt forest -adv
!survival hunt mountains -guidance -fb 2
```

## Server Configuration

Servers can customize hunting with these svars:
- `HuntSpeciesGrasslands` - Grasslands animal data
- `HuntSpeciesMountains` - Mountains animal data
- `HuntSpeciesForest` - Forest animal data
- `HuntArgs` - Custom hunting terrain mappings
- `SurvSettings` - DC thresholds and harvest settings
