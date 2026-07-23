
# Error Exception

Find out more here: [https://developer.xero.com/documentation/api/http-response-codes](https://developer.xero.com/documentation/api/http-response-codes)

## Structure

`ErrorException`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `elements` | [`?(Element[])`](../../doc/models/element.md) | Optional | Array of Elements of validation Errors | getElements(): ?array | setElements(?array elements): void |
| `errorNumber` | `?int` | Optional | Exception number | getErrorNumber(): ?int | setErrorNumber(?int errorNumber): void |
| `message` | `?string` | Optional | Exception message | getMessage(): ?string | setMessage(?string message): void |
| `type` | `?string` | Optional | Exception type | getType(): ?string | setType(?string type): void |

## Example

```php
try {
    // make the API call
} catch (ErrorException $exp) {
    echo 'Caught ErrorException:', $exp;
} catch (ApiException $exp) {
    echo 'Caught ApiException:', $exp;
}
```

