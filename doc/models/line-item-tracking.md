
# Line Item Tracking

Find out more here: [https://developer.xero.com/documentation/api/invoices#post](https://developer.xero.com/documentation/api/invoices#post)

## Structure

`LineItemTracking`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | The name of the tracking category<br><br>**Constraints**: *Maximum Length*: `100` | getName(): ?string | setName(?string name): void |
| `option` | `?string` | Optional | See Tracking Options | getOption(): ?string | setOption(?string option): void |
| `trackingCategoryID` | `?string` | Optional | The Xero identifier for a tracking category | getTrackingCategoryID(): ?string | setTrackingCategoryID(?string trackingCategoryID): void |
| `trackingOptionID` | `?string` | Optional | The Xero identifier for a tracking category option | getTrackingOptionID(): ?string | setTrackingOptionID(?string trackingOptionID): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\LineItemTrackingBuilder;

$lineItemTracking = LineItemTrackingBuilder::init()
    ->name('Region')
    ->option('North')
    ->trackingCategoryID('00000000-0000-0000-0000-000000000000')
    ->trackingOptionID('00000000-0000-0000-0000-000000000000')
    ->build();
```

