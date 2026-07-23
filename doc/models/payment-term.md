
# Payment Term

Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/)

## Structure

`PaymentTerm`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `bills` | [`?Bill`](../../doc/models/bill.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/) | getBills(): ?Bill | setBills(?Bill bills): void |
| `sales` | [`?Bill`](../../doc/models/bill.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/) | getSales(): ?Bill | setSales(?Bill sales): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\PaymentTermBuilder;
use XeroAccountingAPILib\Models\Builders\BillBuilder;
use XeroAccountingAPILib\Models\PaymentTermTypeEnum;

$paymentTerm = PaymentTermBuilder::init()
    ->bills(
        BillBuilder::init()
            ->day(232)
            ->type(PaymentTermTypeEnum::DAYSAFTERBILLDATE)
            ->build()
    )
    ->sales(
        BillBuilder::init()
            ->day(228)
            ->type(PaymentTermTypeEnum::DAYSAFTERBILLDATE)
            ->build()
    )
    ->build();
```

