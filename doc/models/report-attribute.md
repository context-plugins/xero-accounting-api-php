
# Report Attribute

Find out more here: [http://developer.xero.com/documentation/api/reports/](http://developer.xero.com/documentation/api/reports/)

## Structure

`ReportAttribute`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?string` | Optional | - | getId(): ?string | setId(?string id): void |
| `value` | `?string` | Optional | - | getValue(): ?string | setValue(?string value): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ReportAttributeBuilder;

$reportAttribute = ReportAttributeBuilder::init()
    ->id('Id6')
    ->value('Value2')
    ->build();
```

