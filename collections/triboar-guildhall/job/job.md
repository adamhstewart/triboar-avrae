# Job Alias

Work a job to earn gold! Roll a skill check - the better your roll, the more gold you earn.

## Usage

```
!job [skill]
```

- If no skill is specified, Perception is used by default
- You can specify any skill name (e.g., `investigation`, `sleight`, `persuasion`)
- Earnings are calculated as `(skill_roll_total)d4/2` gold pieces
- Gold is automatically added to your coin purse (requires baglib)

## Features

- **Daily Cooldown**: Work once per day, resets at midnight in your timezone
- **Timezone Support**: Set your timezone with `!uvar timezone <UTC_offset>` (e.g., `-5` for EST)
- **Dynamic Descriptions**: Random flavor text based on the skill you use
- **Bag Integration**: Automatically adds earned gold to your coin purse using baglib

## Dependencies

- **baglib**: `5f1ffcbf-3f59-4396-b402-1ca0f02d6bbb`
- **job-descriptions gvar**: `fa47e34f-99b2-4ddf-82a5-302b72010059`

## Examples

```
!job                    # Work using Perception (default)
!job investigation      # Work using Investigation
!job sleight            # Work using Sleight of Hand
!job help               # Show help message
```

## Configuration

### Server Customization

Servers can override job descriptions by setting an svar:
```
!svar jobDescriptions <json>
```

The JSON should follow the same format as the gvar, with skill names as keys and arrays of description strings as values.
