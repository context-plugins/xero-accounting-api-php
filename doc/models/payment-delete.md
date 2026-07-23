
# Payment Delete

Find out more here: [http://developer.xero.com/documentation/api/payments/](http://developer.xero.com/documentation/api/payments/)

## Structure

`PaymentDelete`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `status` | `string` | Required | The status of the payment.<br><br>**Default**: `'DELETED'` | getStatus(): string | setStatus(string status): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\PaymentDeleteBuilder;

$paymentDelete = PaymentDeleteBuilder::init(
    'DELETED'
)->build();
```

