
# Payment Service

Find out more here: [http://developer.xero.com/documentation/api/branding-themes/](http://developer.xero.com/documentation/api/branding-themes/)

## Structure

`PaymentService`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `payNowText` | `?string` | Optional | The text displayed on the Pay Now button in Xero Online Invoicing. If this is not set it will default to Pay by credit card | getPayNowText(): ?string | setPayNowText(?string payNowText): void |
| `paymentServiceID` | `?string` | Optional | Xero identifier | getPaymentServiceID(): ?string | setPaymentServiceID(?string paymentServiceID): void |
| `paymentServiceName` | `?string` | Optional | Name of payment service | getPaymentServiceName(): ?string | setPaymentServiceName(?string paymentServiceName): void |
| `paymentServiceType` | `?string` | Optional | This will always be CUSTOM for payment services created via the API. | getPaymentServiceType(): ?string | setPaymentServiceType(?string paymentServiceType): void |
| `paymentServiceUrl` | `?string` | Optional | The custom payment URL | getPaymentServiceUrl(): ?string | setPaymentServiceUrl(?string paymentServiceUrl): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\PaymentServiceBuilder;

$paymentService = PaymentServiceBuilder::init()
    ->payNowText('PayNowText0')
    ->paymentServiceID('00000e6a-0000-0000-0000-000000000000')
    ->paymentServiceName('PaymentServiceName0')
    ->paymentServiceType('PaymentServiceType0')
    ->paymentServiceUrl('PaymentServiceUrl6')
    ->build();
```

