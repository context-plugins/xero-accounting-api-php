
# Tax Component

Find out more here: [http://developer.xero.com/documentation/api/tax-rates/](http://developer.xero.com/documentation/api/tax-rates/)

## Structure

`TaxComponent`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `isCompound` | `?bool` | Optional | Boolean to describe if Tax rate is compounded. | getIsCompound(): ?bool | setIsCompound(?bool isCompound): void |
| `isNonRecoverable` | `?bool` | Optional | Boolean to describe if tax rate is non-recoverable. Non-recoverable rates are only applicable to Canadian organisations | getIsNonRecoverable(): ?bool | setIsNonRecoverable(?bool isNonRecoverable): void |
| `name` | `?string` | Optional | Name of Tax Component | getName(): ?string | setName(?string name): void |
| `rate` | `?float` | Optional | Tax Rate (up to 4dp) | getRate(): ?float | setRate(?float rate): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\TaxComponentBuilder;

$taxComponent = TaxComponentBuilder::init()
    ->isCompound(false)
    ->isNonRecoverable(false)
    ->name('Name6')
    ->rate(30.52)
    ->build();
```

