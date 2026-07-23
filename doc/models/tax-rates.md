
# Tax Rates

## Structure

`TaxRates`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `taxRates` | [`?(TaxRate[])`](../../doc/models/tax-rate.md) | Optional | - | getTaxRates(): ?array | setTaxRates(?array taxRates): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\TaxRatesBuilder;
use XeroAccountingAPILib\Models\Builders\TaxRateBuilder;

$taxRates = TaxRatesBuilder::init()
    ->taxRates(
        [
            TaxRateBuilder::init()
                ->canApplyToAssets(false)
                ->canApplyToEquity(false)
                ->canApplyToExpenses(false)
                ->canApplyToLiabilities(false)
                ->canApplyToRevenue(false)
                ->build(),
            TaxRateBuilder::init()
                ->canApplyToAssets(false)
                ->canApplyToEquity(false)
                ->canApplyToExpenses(false)
                ->canApplyToLiabilities(false)
                ->canApplyToRevenue(false)
                ->build(),
            TaxRateBuilder::init()
                ->canApplyToAssets(false)
                ->canApplyToEquity(false)
                ->canApplyToExpenses(false)
                ->canApplyToLiabilities(false)
                ->canApplyToRevenue(false)
                ->build()
        ]
    )
    ->build();
```

