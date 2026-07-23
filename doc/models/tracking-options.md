
# Tracking Options

## Structure

`TrackingOptions`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `options` | [`?(TrackingOption[])`](../../doc/models/tracking-option.md) | Optional | - | getOptions(): ?array | setOptions(?array options): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\TrackingOptionsBuilder;
use XeroAccountingAPILib\Models\Builders\TrackingOptionBuilder;
use XeroAccountingAPILib\Models\Status13Enum;

$trackingOptions = TrackingOptionsBuilder::init()
    ->options(
        [
            TrackingOptionBuilder::init()
                ->name('Name2')
                ->status(Status13Enum::ARCHIVED)
                ->trackingCategoryID('00000ecc-0000-0000-0000-000000000000')
                ->trackingOptionID('000009c8-0000-0000-0000-000000000000')
                ->build(),
            TrackingOptionBuilder::init()
                ->name('Name2')
                ->status(Status13Enum::ARCHIVED)
                ->trackingCategoryID('00000ecc-0000-0000-0000-000000000000')
                ->trackingOptionID('000009c8-0000-0000-0000-000000000000')
                ->build(),
            TrackingOptionBuilder::init()
                ->name('Name2')
                ->status(Status13Enum::ARCHIVED)
                ->trackingCategoryID('00000ecc-0000-0000-0000-000000000000')
                ->trackingOptionID('000009c8-0000-0000-0000-000000000000')
                ->build()
        ]
    )
    ->build();
```

