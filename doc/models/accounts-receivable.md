
# Accounts Receivable

## Structure

`AccountsReceivable`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `outstanding` | `?float` | Optional | - | getOutstanding(): ?float | setOutstanding(?float outstanding): void |
| `overdue` | `?float` | Optional | - | getOverdue(): ?float | setOverdue(?float overdue): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\AccountsReceivableBuilder;

$accountsReceivable = AccountsReceivableBuilder::init()
    ->outstanding(29.26)
    ->overdue(160.28)
    ->build();
```

