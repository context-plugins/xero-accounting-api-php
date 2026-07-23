
# Phone

Find out more here: [http://developer.xero.com/documentation/api/types](http://developer.xero.com/documentation/api/types)

## Structure

`Phone`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `phoneAreaCode` | `?string` | Optional | max length = 10<br><br>**Constraints**: *Maximum Length*: `10` | getPhoneAreaCode(): ?string | setPhoneAreaCode(?string phoneAreaCode): void |
| `phoneCountryCode` | `?string` | Optional | max length = 20<br><br>**Constraints**: *Maximum Length*: `20` | getPhoneCountryCode(): ?string | setPhoneCountryCode(?string phoneCountryCode): void |
| `phoneNumber` | `?string` | Optional | max length = 50<br><br>**Constraints**: *Maximum Length*: `50` | getPhoneNumber(): ?string | setPhoneNumber(?string phoneNumber): void |
| `phoneType` | [`?string(PhoneTypeEnum)`](../../doc/models/phone-type-enum.md) | Optional | - | getPhoneType(): ?string | setPhoneType(?string phoneType): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\PhoneBuilder;
use XeroAccountingAPILib\Models\PhoneTypeEnum;

$phone = PhoneBuilder::init()
    ->phoneAreaCode('PhoneAreaCode8')
    ->phoneCountryCode('PhoneCountryCode6')
    ->phoneNumber('PhoneNumber2')
    ->phoneType(PhoneTypeEnum::DEFAULT_)
    ->build();
```

