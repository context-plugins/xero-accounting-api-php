
# Setup

Find out more here: [https://developer.xero.com/documentation/api-guides/conversions](https://developer.xero.com/documentation/api-guides/conversions)

## Structure

`Setup`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accounts` | [`?(Account[])`](../../doc/models/account.md) | Optional | - | getAccounts(): ?array | setAccounts(?array accounts): void |
| `conversionBalances` | [`?(ConversionBalances[])`](../../doc/models/conversion-balances.md) | Optional | Balance supplied for each account that has a value as at the conversion date. | getConversionBalances(): ?array | setConversionBalances(?array conversionBalances): void |
| `conversionDate` | [`?ConversionDate`](../../doc/models/conversion-date.md) | Optional | The date when the organisation starts using Xero | getConversionDate(): ?ConversionDate | setConversionDate(?ConversionDate conversionDate): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\SetupBuilder;
use XeroAccountingAPILib\Models\Builders\AccountBuilder;
use XeroAccountingAPILib\Models\BankAccountTypeEnum;
use XeroAccountingAPILib\Models\ClassEnum;
use XeroAccountingAPILib\Models\Builders\ConversionBalancesBuilder;
use XeroAccountingAPILib\Models\Builders\BalanceDetailsBuilder;
use XeroAccountingAPILib\Models\Builders\ConversionDateBuilder;

$setup = SetupBuilder::init()
    ->accounts(
        [
            AccountBuilder::init()
                ->accountID('000025be-0000-0000-0000-000000000000')
                ->addToWatchlist(false)
                ->bankAccountNumber('BankAccountNumber6')
                ->bankAccountType(BankAccountTypeEnum::BANK)
                ->class(ClassEnum::EQUITY)
                ->build()
        ]
    )
    ->conversionBalances(
        [
            ConversionBalancesBuilder::init()
                ->accountCode('AccountCode6')
                ->balance(44.3)
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
                ->build(),
            ConversionBalancesBuilder::init()
                ->accountCode('AccountCode6')
                ->balance(44.3)
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
                ->build()
        ]
    )
    ->conversionDate(
        ConversionDateBuilder::init()
            ->month(106)
            ->year(68)
            ->build()
    )
    ->build();
```

