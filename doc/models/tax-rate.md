
# Tax Rate

Find out more here: [http://developer.xero.com/documentation/api/tax-rates/](http://developer.xero.com/documentation/api/tax-rates/)

## Structure

`TaxRate`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `canApplyToAssets` | `?bool` | Optional, Read-only | Boolean to describe if tax rate can be used for asset accounts i.e.  true,false | getCanApplyToAssets(): ?bool | setCanApplyToAssets(?bool canApplyToAssets): void |
| `canApplyToEquity` | `?bool` | Optional, Read-only | Boolean to describe if tax rate can be used for equity accounts i.e true,false | getCanApplyToEquity(): ?bool | setCanApplyToEquity(?bool canApplyToEquity): void |
| `canApplyToExpenses` | `?bool` | Optional, Read-only | Boolean to describe if tax rate can be used for expense accounts  i.e. true,false | getCanApplyToExpenses(): ?bool | setCanApplyToExpenses(?bool canApplyToExpenses): void |
| `canApplyToLiabilities` | `?bool` | Optional, Read-only | Boolean to describe if tax rate can be used for liability accounts  i.e. true,false | getCanApplyToLiabilities(): ?bool | setCanApplyToLiabilities(?bool canApplyToLiabilities): void |
| `canApplyToRevenue` | `?bool` | Optional, Read-only | Boolean to describe if tax rate can be used for revenue accounts i.e. true,false | getCanApplyToRevenue(): ?bool | setCanApplyToRevenue(?bool canApplyToRevenue): void |
| `displayTaxRate` | `?float` | Optional, Read-only | Tax Rate (decimal to 4dp) e.g 12.5000 | getDisplayTaxRate(): ?float | setDisplayTaxRate(?float displayTaxRate): void |
| `effectiveRate` | `?float` | Optional, Read-only | Effective Tax Rate (decimal to 4dp) e.g 12.5000 | getEffectiveRate(): ?float | setEffectiveRate(?float effectiveRate): void |
| `name` | `?string` | Optional | Name of tax rate | getName(): ?string | setName(?string name): void |
| `reportTaxType` | [`?string(ReportTaxTypeEnum)`](../../doc/models/report-tax-type-enum.md) | Optional | See ReportTaxTypes | getReportTaxType(): ?string | setReportTaxType(?string reportTaxType): void |
| `status` | [`?string(Status19Enum)`](../../doc/models/status-19-enum.md) | Optional | See Status Codes | getStatus(): ?string | setStatus(?string status): void |
| `taxComponents` | [`?(TaxComponent[])`](../../doc/models/tax-component.md) | Optional | See TaxComponents | getTaxComponents(): ?array | setTaxComponents(?array taxComponents): void |
| `taxType` | `?string` | Optional | The tax type | getTaxType(): ?string | setTaxType(?string taxType): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\TaxRateBuilder;

$taxRate = TaxRateBuilder::init()
    ->canApplyToAssets(false)
    ->canApplyToEquity(false)
    ->canApplyToExpenses(false)
    ->canApplyToLiabilities(false)
    ->canApplyToRevenue(false)
    ->build();
```

