
# Tracking Option

Find out more here: [http://developer.xero.com/documentation/api/tracking-categories/](http://developer.xero.com/documentation/api/tracking-categories/)

## Structure

`TrackingOption`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | The name of the tracking option e.g. Marketing, East (max length = 100)<br><br>**Constraints**: *Maximum Length*: `100` | getName(): ?string | setName(?string name): void |
| `status` | [`?string(Status13Enum)`](../../doc/models/status-13-enum.md) | Optional | The status of a tracking option | getStatus(): ?string | setStatus(?string status): void |
| `trackingCategoryID` | `?string` | Optional | Filter by a tracking category e.g. 297c2dc5-cc47-4afd-8ec8-74990b8761e9 | getTrackingCategoryID(): ?string | setTrackingCategoryID(?string trackingCategoryID): void |
| `trackingOptionID` | `?string` | Optional | The Xero identifier for a tracking option e.g. ae777a87-5ef3-4fa0-a4f0-d10e1f13073a | getTrackingOptionID(): ?string | setTrackingOptionID(?string trackingOptionID): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\TrackingOptionBuilder;
use XeroAccountingAPILib\Models\Status13Enum;

$trackingOption = TrackingOptionBuilder::init()
    ->name('Name6')
    ->status(Status13Enum::ARCHIVED)
    ->trackingCategoryID('0000259e-0000-0000-0000-000000000000')
    ->trackingOptionID('00001a06-0000-0000-0000-000000000000')
    ->build();
```

