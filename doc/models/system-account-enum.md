
# System Account Enum

If this is a system account then this element is returned. See System Account types. Note that non-system accounts may have this element set as either “” or null.

## Enumeration

`SystemAccountEnum`

## Fields

| Name |
|  --- |
| `DEBTORS` |
| `CREDITORS` |
| `BANKCURRENCYGAIN` |
| `GST` |
| `GSTONIMPORTS` |
| `HISTORICAL` |
| `REALISEDCURRENCYGAIN` |
| `RETAINEDEARNINGS` |
| `ROUNDING` |
| `TRACKINGTRANSFERS` |
| `UNPAIDEXPCLM` |
| `UNREALISEDCURRENCYGAIN` |
| `WAGEPAYABLES` |
| `CISASSETS` |
| `CISASSET` |
| `CISLABOUR` |
| `CISLABOUREXPENSE` |
| `CISLABOURINCOME` |
| `CISLIABILITY` |
| `CISMATERIALS` |

## Example

```php
use XeroAccountingAPILib\Models\SystemAccountEnum;

$systemAccount = SystemAccountEnum::CISASSET;
```

