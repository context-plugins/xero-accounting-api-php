
# Actions

## Structure

`Actions`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `actions` | [`?(Action[])`](../../doc/models/action.md) | Optional | - | getActions(): ?array | setActions(?array actions): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ActionsBuilder;
use XeroAccountingAPILib\Models\Builders\ActionBuilder;
use XeroAccountingAPILib\Models\Status1Enum;

$actions = ActionsBuilder::init()
    ->actions(
        [
            ActionBuilder::init()
                ->name('Name4')
                ->status(Status1Enum::ALLOWED)
                ->build(),
            ActionBuilder::init()
                ->name('Name4')
                ->status(Status1Enum::ALLOWED)
                ->build(),
            ActionBuilder::init()
                ->name('Name4')
                ->status(Status1Enum::ALLOWED)
                ->build()
        ]
    )
    ->build();
```

