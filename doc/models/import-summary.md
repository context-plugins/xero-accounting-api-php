
# Import Summary

A summary of the import from setup endpoint

Find out more here: [https://developer.xero.com/documentation/api-guides/conversions](https://developer.xero.com/documentation/api-guides/conversions)

## Structure

`ImportSummary`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accounts` | [`?ImportSummaryAccounts`](../../doc/models/import-summary-accounts.md) | Optional | A summary of the accounts changes | getAccounts(): ?ImportSummaryAccounts | setAccounts(?ImportSummaryAccounts accounts): void |
| `organisation` | [`?ImportSummaryOrganisation`](../../doc/models/import-summary-organisation.md) | Optional | - | getOrganisation(): ?ImportSummaryOrganisation | setOrganisation(?ImportSummaryOrganisation organisation): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ImportSummaryBuilder;
use XeroAccountingAPILib\Models\Builders\ImportSummaryAccountsBuilder;
use XeroAccountingAPILib\Models\Builders\ImportSummaryOrganisationBuilder;

$importSummary = ImportSummaryBuilder::init()
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
    ->build();
```

