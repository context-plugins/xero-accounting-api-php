
# Conversion Balances

Balance supplied for each account that has a value as at the conversion date.

## Structure

`ConversionBalances`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountCode` | `?string` | Optional | The account code for a account | getAccountCode(): ?string | setAccountCode(?string accountCode): void |
| `balance` | `?float` | Optional | The opening balances of the account. Debits are positive, credits are negative values | getBalance(): ?float | setBalance(?float balance): void |
| `balanceDetails` | [`?(BalanceDetails[])`](../../doc/models/balance-details.md) | Optional | - | getBalanceDetails(): ?array | setBalanceDetails(?array balanceDetails): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ConversionBalancesBuilder;
use XeroAccountingAPILib\Models\Builders\BalanceDetailsBuilder;

$conversionBalances = ConversionBalancesBuilder::init()
    ->accountCode('AccountCode0')
    ->balance(134.94)
    ->balanceDetails(
        [
            BalanceDetailsBuilder::init()
                ->balance(162.9)
                ->currencyCode('CurrencyCode2')
                ->currencyRate(208.22)
                ->build(),
            BalanceDetailsBuilder::init()
                ->balance(162.9)
                ->currencyCode('CurrencyCode2')
                ->currencyRate(208.22)
                ->build()
        ]
    )
    ->build();
```

