
# Import Summary Accounts

A summary of the accounts changes

## Structure

`ImportSummaryAccounts`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `deleted` | `?float` | Optional | The number of accounts deleted | getDeleted(): ?float | setDeleted(?float deleted): void |
| `errored` | `?float` | Optional | The number of accounts that had an error | getErrored(): ?float | setErrored(?float errored): void |
| `locked` | `?float` | Optional | The number of locked accounts | getLocked(): ?float | setLocked(?float locked): void |
| `new` | `?float` | Optional | The number of new accounts created | getNew(): ?float | setNew(?float new): void |
| `newOrUpdated` | `?float` | Optional | The number of new or updated accounts | getNewOrUpdated(): ?float | setNewOrUpdated(?float newOrUpdated): void |
| `present` | `?bool` | Optional | - | getPresent(): ?bool | setPresent(?bool present): void |
| `system` | `?float` | Optional | The number of system accounts | getSystem(): ?float | setSystem(?float system): void |
| `total` | `?float` | Optional | The total number of accounts in the org | getTotal(): ?float | setTotal(?float total): void |
| `updated` | `?float` | Optional | The number of accounts updated | getUpdated(): ?float | setUpdated(?float updated): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ImportSummaryAccountsBuilder;

$importSummaryAccounts = ImportSummaryAccountsBuilder::init()
    ->deleted(1.34)
    ->errored(4.08)
    ->locked(62.36)
    ->new(187.5)
    ->newOrUpdated(191.98)
    ->build();
```

