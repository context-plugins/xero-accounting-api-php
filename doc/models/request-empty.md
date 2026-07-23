
# Request Empty

Find out more here: [http://developer.xero.com/documentation/api/invoice/](http://developer.xero.com/documentation/api/invoice/)

## Structure

`RequestEmpty`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `status` | `?string` | Optional | Need at least one field to create an empty JSON payload | getStatus(): ?string | setStatus(?string status): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\RequestEmptyBuilder;

$requestEmpty = RequestEmptyBuilder::init()
    ->status('Status8')
    ->build();
```

