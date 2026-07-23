
# Due Date Type Enum

the payment terms

## Enumeration

`DueDateTypeEnum`

## Fields

| Name |
|  --- |
| `DAYSAFTERBILLDATE` |
| `DAYSAFTERBILLMONTH` |
| `DAYSAFTERINVOICEDATE` |
| `DAYSAFTERINVOICEMONTH` |
| `OFCURRENTMONTH` |
| `OFFOLLOWINGMONTH` |

## Example

```php
use XeroAccountingAPILib\Models\DueDateTypeEnum;

$dueDateType = DueDateTypeEnum::DAYSAFTERINVOICEDATE;
```

