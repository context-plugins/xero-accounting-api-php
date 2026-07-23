
# Sales Tax Period Enum

The frequency with which tax returns are processed. See Sales Tax Period

## Enumeration

`SalesTaxPeriodEnum`

## Fields

| Name |
|  --- |
| `MONTHLY` |
| `QUARTERLY1` |
| `QUARTERLY2` |
| `QUARTERLY3` |
| `ANNUALLY` |
| `ONEMONTHS` |
| `TWOMONTHS` |
| `SIXMONTHS` |
| `ENUM_1MONTHLY` |
| `ENUM_2MONTHLY` |
| `ENUM_3MONTHLY` |
| `ENUM_6MONTHLY` |
| `QUARTERLY` |
| `YEARLY` |
| `NONE` |

## Example

```php
use XeroAccountingAPILib\Models\SalesTaxPeriodEnum;

$salesTaxPeriod = SalesTaxPeriodEnum::ENUM_2MONTHLY;
```

