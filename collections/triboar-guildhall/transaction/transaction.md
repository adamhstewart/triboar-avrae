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

## Notes

- Positive values add currency to your purse
- Negative values subtract currency from your purse
- The alias displays the full coin purse breakdown after the transaction
- Tool proficiencies are shown for quick reference during crafting or other activities
