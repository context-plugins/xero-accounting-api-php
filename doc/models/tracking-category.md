
# Tracking Category

Find out more here: [http://developer.xero.com/documentation/api/tracking-categories/](http://developer.xero.com/documentation/api/tracking-categories/)

## Structure

`TrackingCategory`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | The name of the tracking category e.g. Department, Region (max length = 100)<br><br>**Constraints**: *Maximum Length*: `100` | getName(): ?string | setName(?string name): void |
| `option` | `?string` | Optional | The option name of the tracking option e.g. East, West (max length = 100)<br><br>**Constraints**: *Maximum Length*: `100` | getOption(): ?string | setOption(?string option): void |
| `options` | [`?(TrackingOption[])`](../../doc/models/tracking-option.md) | Optional | See Tracking Options | getOptions(): ?array | setOptions(?array options): void |
| `status` | [`?string(Status14Enum)`](../../doc/models/status-14-enum.md) | Optional | The status of a tracking category | getStatus(): ?string | setStatus(?string status): void |
| `trackingCategoryID` | `?string` | Optional | The Xero identifier for a tracking category e.g. 297c2dc5-cc47-4afd-8ec8-74990b8761e9 | getTrackingCategoryID(): ?string | setTrackingCategoryID(?string trackingCategoryID): void |
| `trackingOptionID` | `?string` | Optional | The Xero identifier for a tracking option e.g. dc54c220-0140-495a-b925-3246adc0075f | getTrackingOptionID(): ?string | setTrackingOptionID(?string trackingOptionID): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\TrackingCategoryBuilder;
use XeroAccountingAPILib\Models\Builders\TrackingOptionBuilder;
use XeroAccountingAPILib\Models\Status13Enum;
use XeroAccountingAPILib\Models\Status14Enum;

$trackingCategory = TrackingCategoryBuilder::init()
    ->name('Name4')
    ->option('Option4')
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
                ->build()
        ]
    )
    ->status(Status14Enum::DELETED)
    ->trackingCategoryID('000024cc-0000-0000-0000-000000000000')
    ->build();
```

