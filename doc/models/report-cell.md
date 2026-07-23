
# Report Cell

## Structure

`ReportCell`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `attributes` | [`?(ReportAttribute[])`](../../doc/models/report-attribute.md) | Optional | - | getAttributes(): ?array | setAttributes(?array attributes): void |
| `value` | `?string` | Optional | - | getValue(): ?string | setValue(?string value): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ReportCellBuilder;
use XeroAccountingAPILib\Models\Builders\ReportAttributeBuilder;

$reportCell = ReportCellBuilder::init()
    ->attributes(
        [
            ReportAttributeBuilder::init()
                ->id('Id4')
                ->value('Value6')
                ->build()
        ]
    )
    ->value('Value0')
    ->build();
```

