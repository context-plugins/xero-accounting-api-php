
# Line Amount Types Enum

Line amounts are exclusive of tax by default if you don’t specify this element. See Line Amount Types

## Enumeration

`LineAmountTypesEnum`

## Fields

| Name |
|  --- |
| `EXCLUSIVE` |
| `INCLUSIVE` |
| `NOTAX` |

## Example

```php
use XeroAccountingAPILib\Models\LineAmountTypesEnum;

$lineAmountTypes = LineAmountTypesEnum::EXCLUSIVE;
```

