
# CIS Org Setting

Find out more here: [https://developer.xero.com/documentation/api/organisation](https://developer.xero.com/documentation/api/organisation)

## Structure

`CISOrgSetting`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cISContractorEnabled` | `?bool` | Optional | true or false - Boolean that describes if the organisation is a CIS Contractor | getCISContractorEnabled(): ?bool | setCISContractorEnabled(?bool cISContractorEnabled): void |
| `cISSubContractorEnabled` | `?bool` | Optional | true or false - Boolean that describes if the organisation is a CIS SubContractor | getCISSubContractorEnabled(): ?bool | setCISSubContractorEnabled(?bool cISSubContractorEnabled): void |
| `rate` | `?float` | Optional, Read-only | CIS Deduction rate for the organisation | getRate(): ?float | setRate(?float rate): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\CISOrgSettingBuilder;

$cISOrgSetting = CISOrgSettingBuilder::init()
    ->cISContractorEnabled(false)
    ->cISSubContractorEnabled(false)
    ->rate(58.56)
    ->build();
```

