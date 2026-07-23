
# Import Summary Organisation

## Structure

`ImportSummaryOrganisation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `present` | `?bool` | Optional | - | getPresent(): ?bool | setPresent(?bool present): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ImportSummaryOrganisationBuilder;

$importSummaryOrganisation = ImportSummaryOrganisationBuilder::init()
    ->present(false)
    ->build();
```

