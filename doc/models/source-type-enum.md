
# Source Type Enum

The journal source type. The type of transaction that created the journal

## Enumeration

`SourceTypeEnum`

## Fields

| Name |
|  --- |
| `ACCREC` |
| `ACCPAY` |
| `ACCRECCREDIT` |
| `ACCPAYCREDIT` |
| `ACCRECPAYMENT` |
| `ACCPAYPAYMENT` |
| `ARCREDITPAYMENT` |
| `APCREDITPAYMENT` |
| `CASHREC` |
| `CASHPAID` |
| `TRANSFER` |
| `ARPREPAYMENT` |
| `APPREPAYMENT` |
| `AROVERPAYMENT` |
| `APOVERPAYMENT` |
| `EXPCLAIM` |
| `EXPPAYMENT` |
| `MANJOURNAL` |
| `PAYSLIP` |
| `WAGEPAYABLE` |
| `INTEGRATEDPAYROLLPE` |
| `INTEGRATEDPAYROLLPT` |
| `EXTERNALSPENDMONEY` |
| `INTEGRATEDPAYROLLPTPAYMENT` |
| `INTEGRATEDPAYROLLCN` |

## Example

```php
use XeroAccountingAPILib\Models\SourceTypeEnum;

$sourceType = SourceTypeEnum::INTEGRATEDPAYROLLPT;
```

