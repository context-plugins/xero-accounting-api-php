
# Payment Services

## Structure

`PaymentServices`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `paymentServices` | [`?(PaymentService[])`](../../doc/models/payment-service.md) | Optional | - | getPaymentServices(): ?array | setPaymentServices(?array paymentServices): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\PaymentServicesBuilder;
use XeroAccountingAPILib\Models\Builders\PaymentServiceBuilder;

$paymentServices = PaymentServicesBuilder::init()
    ->paymentServices(
        [
            PaymentServiceBuilder::init()
                ->payNowText('PayNowText4')
                ->paymentServiceID('00000ed4-0000-0000-0000-000000000000')
                ->paymentServiceName('PaymentServiceName4')
                ->paymentServiceType('PaymentServiceType4')
                ->paymentServiceUrl('PaymentServiceUrl0')
                ->build(),
            PaymentServiceBuilder::init()
                ->payNowText('PayNowText4')
                ->paymentServiceID('00000ed4-0000-0000-0000-000000000000')
                ->paymentServiceName('PaymentServiceName4')
                ->paymentServiceType('PaymentServiceType4')
                ->paymentServiceUrl('PaymentServiceUrl0')
                ->build(),
            PaymentServiceBuilder::init()
                ->payNowText('PayNowText4')
                ->paymentServiceID('00000ed4-0000-0000-0000-000000000000')
                ->paymentServiceName('PaymentServiceName4')
                ->paymentServiceType('PaymentServiceType4')
                ->paymentServiceUrl('PaymentServiceUrl0')
                ->build()
        ]
    )
    ->build();
```

