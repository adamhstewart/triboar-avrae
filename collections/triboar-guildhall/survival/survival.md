# Survival Alias

A collection of wilderness survival activities for gathering food and resources.

## Subcommands

The survival alias provides access to three main activities:

### Hunt
Hunt for game in various terrains (grasslands, mountains, forest).

```
!survival hunt <terrain>
!survival hunt help
```

### Fish
Fish in different water bodies (river, lake, sea).

```
!survival fish <location>
!survival fish help
```

### Forage
Forage for edible plants and food in different environments (grasslands, mountains, forest).

```
!survival forage <terrain>
!survival forage help
```

## Usage

Use `!survival` to see general help, or use the individual subcommand help for detailed information:
- `!survival hunt help`
- `!survival fish help`
- `!survival forage help`

## Features

Each survival activity involves:
- Finding the resource (skill check)
- Gathering/catching it (skill check or attack roll)
- Harvesting it (skill check)
- Adding resources to your inventory

## Examples

```
!survival hunt grasslands
!survival fish river
!survival forage forest
!survival
```

## Server Configuration

Server admins can customize the survival system using these svars:

### Channel Restrictions
Restrict where each survival activity can be used:
- `FishChannels` - Comma-separated channel IDs for fishing (e.g., `1234567890,9876543210`)
- `HuntChannels` - Comma-separated channel IDs for hunting
- `ForageChannels` - Comma-separated channel IDs for foraging

If not set, activities can be used in any channel.

### Species/Resource Data
Customize what can be found in each location:
- **Fishing:** `FishSpeciesRiver`, `FishSpeciesLake`, `FishSpeciesSea`
- **Hunting:** `HuntSpeciesGrasslands`, `HuntSpeciesMountains`, `HuntSpeciesForest`
- **Foraging:** `ForageSpeciesGrasslands`, `ForageSpeciesMountains`, `ForageSpeciesForest`

### Custom Locations
Add custom locations beyond the defaults:
- `FishArgs` - Map custom fishing locations to species data
- `HuntArgs` - Map custom terrains to species data (shared with forage)

### General Settings
- `SurvSettings` - JSON containing DC thresholds, harvest settings, and cooldown configuration

See individual subcommand documentation for more details.
