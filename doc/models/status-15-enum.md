
# Status 15 Enum

Filter by the combination of ContactID and Status. Get all the linked transactions that have been assigned to a particular customer and have a particular status e.g. GET /LinkedTransactions?ContactID=4bb34b03-3378-4bb2-a0ed-6345abf3224e&Status=APPROVED.

## Enumeration

`Status15Enum`

## Fields

| Name |
|  --- |
| `APPROVED` |
| `DRAFT` |
| `ONDRAFT` |
| `BILLED` |
| `VOIDED` |

## Example

```php
use XeroAccountingAPILib\Models\Status15Enum;

$status15 = Status15Enum::ONDRAFT;
```

