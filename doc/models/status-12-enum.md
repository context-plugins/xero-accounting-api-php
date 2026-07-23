
# Status 12 Enum

Current status of an expense claim – see status types

## Enumeration

`Status12Enum`

## Fields

| Name |
|  --- |
| `SUBMITTED` |
| `AUTHORISED` |
| `PAID` |
| `VOIDED` |
| `DELETED` |

## Example

```php
use XeroAccountingAPILib\Models\Status12Enum;

$status12 = Status12Enum::VOIDED;
```

