
# Type 5 Enum

See Bank Transaction Types

## Enumeration

`Type5Enum`

## Fields

| Name |
|  --- |
| `RECEIVE` |
| `RECEIVEOVERPAYMENT` |
| `RECEIVEPREPAYMENT` |
| `SPEND` |
| `SPENDOVERPAYMENT` |
| `SPENDPREPAYMENT` |
| `RECEIVETRANSFER` |
| `SPENDTRANSFER` |

## Example

```php
use XeroAccountingAPILib\Models\Type5Enum;

$type5 = Type5Enum::RECEIVETRANSFER;
```

