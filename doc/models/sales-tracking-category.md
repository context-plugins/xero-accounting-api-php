
# Sales Tracking Category

Find out more here: [http://developer.xero.com/documentation/api/tracking-categories/](http://developer.xero.com/documentation/api/tracking-categories/)

## Structure

`SalesTrackingCategory`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `trackingCategoryName` | `?string` | Optional | The default sales tracking category name for contacts | getTrackingCategoryName(): ?string | setTrackingCategoryName(?string trackingCategoryName): void |
| `trackingOptionName` | `?string` | Optional | The default purchase tracking category name for contacts | getTrackingOptionName(): ?string | setTrackingOptionName(?string trackingOptionName): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\SalesTrackingCategoryBuilder;

$salesTrackingCategory = SalesTrackingCategoryBuilder::init()
    ->trackingCategoryName('TrackingCategoryName0')
    ->trackingOptionName('TrackingOptionName8')
    ->build();
```

