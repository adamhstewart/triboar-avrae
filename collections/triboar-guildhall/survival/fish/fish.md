# Fish (Survival Subalias)

Fish in rivers, lakes, and seas to catch fish for food.

## Usage

```
!survival fish <location> [options]
!survival fish help
```

## Locations

- **river** - Fish in rivers for freshwater fish
- **lake** - Fish in lakes for different freshwater species
- **sea** - Fish in the ocean for saltwater fish

Servers may configure additional custom fishing locations.

## How It Works

Fishing is a three-step process:

1. **Find a Spot** (Nature check) - Locate a good fishing spot
2. **Catch the Fish** (Survival check) - Hook and reel in the fish
3. **Harvest** (Survival check) - Clean and prepare the fish meat

## Options

- **-adv/-dis** - Roll with advantage/disadvantage
- **-fadv/-fdis** - Advantage/disadvantage on finding a spot
- **-cadv/-cdis** - Advantage/disadvantage on catching
- **-hadv/-hdis** - Advantage/disadvantage on harvesting
- **-b [bonus]** - Add bonus to all rolls
- **-fb/-cb/-hb [bonus]** - Add bonus to specific rolls
- **-guidance** - Add 1d4 guidance to find/harvest rolls
- **-bless** - Add 1d4 bless to catch roll

## Features

- Different fish species per location
- Weight and DC vary by fish type
- Automatic harvesting by default
- Background features may provide bonuses
- Results added to inventory

## Examples

```
!survival fish river
!survival fish sea -adv
!survival fish lake -guidance -fb 2
```

## Server Configuration

Servers can customize fishing with these svars:
- `FishSpeciesRiver` - River fish data
- `FishSpeciesLake` - Lake fish data
- `FishSpeciesSea` - Sea fish data
- `FishArgs` - Custom fishing location mappings
- `SurvSettings` - DC thresholds and harvest settings
