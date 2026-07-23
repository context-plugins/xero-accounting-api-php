
# Balance Details

An array to specify multiple currency balances of an account

## Structure

`BalanceDetails`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `balance` | `?float` | Optional | The opening balances of the account. Debits are positive, credits are negative values | getBalance(): ?float | setBalance(?float balance): void |
| `currencyCode` | `?string` | Optional | The currency of the balance (Not required for base currency) | getCurrencyCode(): ?string | setCurrencyCode(?string currencyCode): void |
| `currencyRate` | `?float` | Optional | (Optional) Exchange rate to base currency when money is spent or received. If not specified, XE rate for the day is applied | getCurrencyRate(): ?float | setCurrencyRate(?float currencyRate): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\BalanceDetailsBuilder;

$balanceDetails = BalanceDetailsBuilder::init()
    ->balance(101.08)
    ->currencyCode('CurrencyCode0')
    ->currencyRate(146.4)
    ->build();
```

