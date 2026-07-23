
# Currencies

## Structure

`Currencies`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `currencies` | [`?(Currency[])`](../../doc/models/currency.md) | Optional | - | getCurrencies(): ?array | setCurrencies(?array currencies): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\CurrenciesBuilder;
use XeroAccountingAPILib\Models\Builders\CurrencyBuilder;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;

$currencies = CurrenciesBuilder::init()
    ->currencies(
        [
            CurrencyBuilder::init()
                ->code(CurrencyCodeEnum::BWP)
                ->description('Description4')
                ->build(),
            CurrencyBuilder::init()
                ->code(CurrencyCodeEnum::BWP)
                ->description('Description4')
                ->build()
        ]
    )
    ->build();
```

