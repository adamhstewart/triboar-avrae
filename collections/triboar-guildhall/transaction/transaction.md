# Transaction Alias

Record transactions and update your coin purse with support for all D&D currency types.

## Usage

```
!transaction "description" -cost1 -cost2 ...
```

- Description can be provided as the first argument or with `-d` or `-desc`
- Add any number of currency amounts (positive to gain, negative to spend)
- Supported currencies: `cp`, `sp`, `ep`, `gp`, `pp`
- Defaults to `gp` if no unit is specified

## Features

- **Multi-Currency Support**: Handle copper, silver, electrum, gold, and platinum
- **Flexible Format**: Mix different currencies in a single transaction
- **Bag Integration**: Automatically updates your coin purse using baglib
- **Tool Proficiency Display**: Shows your tool proficiencies and expertise
- **Character Sheet Link**: Includes a link to your character sheet
- **Channel Restriction**: Can be limited to specific channels by server admins (optional)

## Dependencies

- **baglib**: `5f1ffcbf-3f59-4396-b402-1ca0f02d6bbb`
- **tool_check module**: `6251e20c-7545-4c63-92af-31e0745f2b0c`

## Examples

```
!transaction "4x Potions of Healing" -50gp -50gp -50gp -50gp
!transaction "Sold old armor" 25gp
!transaction "Mixed payment" -10gp -50sp 5cp
!transaction -d "Inn stay" -5gp
!transaction "Found treasure" 100gp 50sp 25cp
```

## Server Configuration

Admins can optionally restrict the transaction command to specific channels using an svar:

```
!svar transactionChannels <channel_id>
```

For multiple channels, separate with commas:
```
!svar transactionChannels 1432009144403230901, 1234567890123456789
```

If the `transactionChannels` svar is not set, the command can be used in any channel.

## Notes

- Positive values add currency to your purse
- Negative values subtract currency from your purse
- The alias displays the full coin purse breakdown after the transaction
- Tool proficiencies are shown for quick reference during crafting or other activities
- A link to your character sheet is included in the embed
