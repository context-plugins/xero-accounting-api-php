
# Currency

Find out more here: [http://developer.xero.com/documentation/api/currencies/](http://developer.xero.com/documentation/api/currencies/)

## Structure

`Currency`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `code` | [`?string(CurrencyCodeEnum)`](../../doc/models/currency-code-enum.md) | Optional | 3 letter alpha code for the currency – see list of currency codes | getCode(): ?string | setCode(?string code): void |
| `description` | `?string` | Optional | Name of Currency | getDescription(): ?string | setDescription(?string description): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\CurrencyBuilder;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;

$currency = CurrencyBuilder::init()
    ->code(CurrencyCodeEnum::BSD)
    ->description('Description6')
    ->build();
```

