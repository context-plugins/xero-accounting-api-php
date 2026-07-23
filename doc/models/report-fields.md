
# Report Fields

## Structure

`ReportFields`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | - | getDescription(): ?string | setDescription(?string description): void |
| `fieldID` | `?string` | Optional | - | getFieldID(): ?string | setFieldID(?string fieldID): void |
| `value` | `?string` | Optional | - | getValue(): ?string | setValue(?string value): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ReportFieldsBuilder;

$reportFields = ReportFieldsBuilder::init()
    ->description('Description6')
    ->fieldID('FieldID0')
    ->value('Value0')
    ->build();
```

