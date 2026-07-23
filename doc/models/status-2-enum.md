
# Status 2 Enum

The Status of a contact group. To delete a contact group update the status to DELETED. Only contact groups with a status of ACTIVE are returned on GETs.

## Enumeration

`Status2Enum`

## Fields

| Name |
|  --- |
| `ACTIVE` |
| `DELETED` |

## Example

```php
use XeroAccountingAPILib\Models\Status2Enum;

$status2 = Status2Enum::ACTIVE;
```

