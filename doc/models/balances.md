
# Balances

The raw AccountsReceivable(sales invoices) and AccountsPayable(bills) outstanding and overdue amounts, not converted to base currency (read only)

## Structure

`Balances`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountsPayable` | [`?AccountsPayable`](../../doc/models/accounts-payable.md) | Optional | - | getAccountsPayable(): ?AccountsPayable | setAccountsPayable(?AccountsPayable accountsPayable): void |
| `accountsReceivable` | [`?AccountsReceivable`](../../doc/models/accounts-receivable.md) | Optional | - | getAccountsReceivable(): ?AccountsReceivable | setAccountsReceivable(?AccountsReceivable accountsReceivable): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\BalancesBuilder;
use XeroAccountingAPILib\Models\Builders\AccountsPayableBuilder;
use XeroAccountingAPILib\Models\Builders\AccountsReceivableBuilder;

$balances = BalancesBuilder::init()
    ->accountsPayable(
        AccountsPayableBuilder::init()
            ->outstanding(161.92)
            ->overdue(36.94)
            ->build()
    )
    ->accountsReceivable(
        AccountsReceivableBuilder::init()
            ->outstanding(82)
            ->overdue(213.02)
            ->build()
    )
    ->build();
```

