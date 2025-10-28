# Price Lookup Alias

Look up item prices, rarity, type, and crafting information from the approved items database.

## Usage

```
!price <item name>
```

- Search for any item by name (partial matches work)
- View detailed information including price, rarity, type, and crafting requirements

## Features

- **Fuzzy Search**: Finds items with partial name matches
- **Smart Results**: Shows single item details or lists multiple matches
- **Crafting Info**: Displays if an item is craftable and what tools are required
- **Large Database**: 800+ approved items from the Triboar Guildhall


## Dependencies

- **item-prices gvar**: Contains the full item database (813 items)

## Examples

```
!price Bag of Holding           # Find a specific item
!price potion                   # Find all potions
!price sword                    # Find all swords
!price help                     # Show help
```

## Output

For a single match, displays:
- Item Name (as title)
- Type
- Rarity
- Cost
- Craftable (Yes/No)
- Tools Required (if craftable)

For multiple matches, shows a list with name, rarity, and cost for each item.
