
# Validation Error

Find out more here: [https://developer.xero.com/documentation/api/http-response-codes](https://developer.xero.com/documentation/api/http-response-codes)

## Structure

`ValidationError`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `message` | `?string` | Optional | Validation error message | getMessage(): ?string | setMessage(?string message): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ValidationErrorBuilder;

$validationError = ValidationErrorBuilder::init()
    ->message('Message4')
    ->build();
```

