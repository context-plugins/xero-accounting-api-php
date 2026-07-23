
# Bill

Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/)

## Structure

`Bill`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `day` | `?int` | Optional | Day of Month (0-31) | getDay(): ?int | setDay(?int day): void |
| `type` | [`?string(PaymentTermTypeEnum)`](../../doc/models/payment-term-type-enum.md) | Optional | - | getType(): ?string | setType(?string type): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\BillBuilder;
use XeroAccountingAPILib\Models\PaymentTermTypeEnum;

$bill = BillBuilder::init()
    ->day(214)
    ->type(PaymentTermTypeEnum::OFCURRENTMONTH)
    ->build();
```

