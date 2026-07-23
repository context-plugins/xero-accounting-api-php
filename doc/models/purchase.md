
# Purchase

Find out more here: [http://developer.xero.com/documentation/api/items/](http://developer.xero.com/documentation/api/items/)

## Structure

`Purchase`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountCode` | `?string` | Optional | Default account code to be used for purchased/sale. Not applicable to the purchase details of tracked items | getAccountCode(): ?string | setAccountCode(?string accountCode): void |
| `cOGSAccountCode` | `?string` | Optional | Cost of goods sold account. Only applicable to the purchase details of tracked items. | getCOGSAccountCode(): ?string | setCOGSAccountCode(?string cOGSAccountCode): void |
| `taxType` | `?string` | Optional | The tax type from TaxRates | getTaxType(): ?string | setTaxType(?string taxType): void |
| `unitPrice` | `?float` | Optional | Unit Price of the item. By default UnitPrice is rounded to two decimal places. You can use 4 decimal places by adding the unitdp=4 querystring parameter to your request. | getUnitPrice(): ?float | setUnitPrice(?float unitPrice): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\PurchaseBuilder;

$purchase = PurchaseBuilder::init()
    ->accountCode('AccountCode8')
    ->cOGSAccountCode('COGSAccountCode0')
    ->taxType('TaxType2')
    ->unitPrice(70.48)
    ->build();
```

