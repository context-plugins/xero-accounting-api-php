
# Quote Line Amount Types Enum

Line amounts are exclusive of tax by default if you don’t specify this element. See Line Amount Types

## Enumeration

`QuoteLineAmountTypesEnum`

## Fields

| Name |
|  --- |
| `EXCLUSIVE` |
| `INCLUSIVE` |
| `NOTAX` |

## Example

```php
use XeroAccountingAPILib\Models\QuoteLineAmountTypesEnum;

$quoteLineAmountTypes = QuoteLineAmountTypesEnum::INCLUSIVE;
```

