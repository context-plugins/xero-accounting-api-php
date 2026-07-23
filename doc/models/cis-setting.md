
# CIS Setting

Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/)

## Structure

`CISSetting`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cISEnabled` | `?bool` | Optional | Boolean that describes if the contact is a CIS Subcontractor | getCISEnabled(): ?bool | setCISEnabled(?bool cISEnabled): void |
| `rate` | `?float` | Optional, Read-only | CIS Deduction rate for the contact if he is a subcontractor. If the contact is not CISEnabled, then the rate is not returned | getRate(): ?float | setRate(?float rate): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\CISSettingBuilder;

$cISSetting = CISSettingBuilder::init()
    ->cISEnabled(false)
    ->rate(100.68)
    ->build();
```

