
# Class 1 Enum

Organisation Classes describe which plan the Xero organisation is on (e.g. DEMO, TRIAL, PREMIUM)

## Enumeration

`Class1Enum`

## Fields

| Name |
|  --- |
| `DEMO` |
| `TRIAL` |
| `STARTER` |
| `STANDARD` |
| `PREMIUM` |
| `PREMIUM_20` |
| `PREMIUM_50` |
| `PREMIUM_100` |
| `LEDGER` |
| `GST_CASHBOOK` |
| `NON_GST_CASHBOOK` |

## Example

```php
use XeroAccountingAPILib\Models\Class1Enum;

$class1 = Class1Enum::TRIAL;
```

