
# Accounts Payable

## Structure

`AccountsPayable`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `outstanding` | `?float` | Optional | - | getOutstanding(): ?float | setOutstanding(?float outstanding): void |
| `overdue` | `?float` | Optional | - | getOverdue(): ?float | setOverdue(?float overdue): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\AccountsPayableBuilder;

$accountsPayable = AccountsPayableBuilder::init()
    ->outstanding(79.98)
    ->overdue(211)
    ->build();
```

