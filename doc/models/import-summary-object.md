
# Import Summary Object

Find out more here: [https://developer.xero.com/documentation/api-guides/conversions](https://developer.xero.com/documentation/api-guides/conversions)

## Structure

`ImportSummaryObject`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `importSummary` | [`?ImportSummary`](../../doc/models/import-summary.md) | Optional | A summary of the import from setup endpoint<br><br>Find out more here: [https://developer.xero.com/documentation/api-guides/conversions](https://developer.xero.com/documentation/api-guides/conversions)<br><br>Find out more here: [https://developer.xero.com/documentation/api-guides/conversions](https://developer.xero.com/documentation/api-guides/conversions) | getImportSummary(): ?ImportSummary | setImportSummary(?ImportSummary importSummary): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ImportSummaryObjectBuilder;
use XeroAccountingAPILib\Models\Builders\ImportSummaryBuilder;
use XeroAccountingAPILib\Models\Builders\ImportSummaryAccountsBuilder;
use XeroAccountingAPILib\Models\Builders\ImportSummaryOrganisationBuilder;

$importSummaryObject = ImportSummaryObjectBuilder::init()
    ->importSummary(
        ImportSummaryBuilder::init()
            ->accounts(
                ImportSummaryAccountsBuilder::init()
                    ->deleted(162.64)
                    ->errored(168.06)
                    ->locked(226.34)
                    ->new(232.48)
                    ->newOrUpdated(228)
                    ->build()
            )
            ->organisation(
                ImportSummaryOrganisationBuilder::init()
                    ->present(false)
                    ->build()
            )
            ->build()
    )
    ->build();
```

