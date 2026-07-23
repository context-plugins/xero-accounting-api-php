
# Items

## Structure

`Items`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `items` | [`?(Item[])`](../../doc/models/item.md) | Optional | - | getItems(): ?array | setItems(?array items): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ItemsBuilder;
use XeroAccountingAPILib\Models\Builders\ItemBuilder;

$items = ItemsBuilder::init()
    ->items(
        [
            ItemBuilder::init(
                'Code0'
            )
                ->description('Description6')
                ->inventoryAssetAccountCode('InventoryAssetAccountCode4')
                ->isPurchased(false)
                ->isSold(false)
                ->isTrackedAsInventory(false)
                ->build(),
            ItemBuilder::init(
                'Code0'
            )
                ->description('Description6')
                ->inventoryAssetAccountCode('InventoryAssetAccountCode4')
                ->isPurchased(false)
                ->isSold(false)
                ->isTrackedAsInventory(false)
                ->build()
        ]
    )
    ->build();
```

