
# Address for Organisation

Find out more here: [http://developer.xero.com/documentation/api/types](http://developer.xero.com/documentation/api/types)

## Structure

`AddressForOrganisation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `addressLine1` | `?string` | Optional | max length = 500<br><br>**Constraints**: *Maximum Length*: `500` | getAddressLine1(): ?string | setAddressLine1(?string addressLine1): void |
| `addressLine2` | `?string` | Optional | max length = 500<br><br>**Constraints**: *Maximum Length*: `500` | getAddressLine2(): ?string | setAddressLine2(?string addressLine2): void |
| `addressLine3` | `?string` | Optional | max length = 500<br><br>**Constraints**: *Maximum Length*: `500` | getAddressLine3(): ?string | setAddressLine3(?string addressLine3): void |
| `addressLine4` | `?string` | Optional | max length = 500<br><br>**Constraints**: *Maximum Length*: `500` | getAddressLine4(): ?string | setAddressLine4(?string addressLine4): void |
| `addressType` | [`?string(AddressType1Enum)`](../../doc/models/address-type-1-enum.md) | Optional | define the type of address | getAddressType(): ?string | setAddressType(?string addressType): void |
| `attentionTo` | `?string` | Optional | max length = 255<br><br>**Constraints**: *Maximum Length*: `255` | getAttentionTo(): ?string | setAttentionTo(?string attentionTo): void |
| `city` | `?string` | Optional | max length = 255<br><br>**Constraints**: *Maximum Length*: `255` | getCity(): ?string | setCity(?string city): void |
| `country` | `?string` | Optional | max length = 50, [A-Z], [a-z] only<br><br>**Constraints**: *Maximum Length*: `50` | getCountry(): ?string | setCountry(?string country): void |
| `postalCode` | `?string` | Optional | max length = 50<br><br>**Constraints**: *Maximum Length*: `50` | getPostalCode(): ?string | setPostalCode(?string postalCode): void |
| `region` | `?string` | Optional | max length = 255<br><br>**Constraints**: *Maximum Length*: `255` | getRegion(): ?string | setRegion(?string region): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\AddressForOrganisationBuilder;
use XeroAccountingAPILib\Models\AddressType1Enum;

$addressForOrganisation = AddressForOrganisationBuilder::init()
    ->addressLine1('AddressLine16')
    ->addressLine2('AddressLine28')
    ->addressLine3('AddressLine30')
    ->addressLine4('AddressLine46')
    ->addressType(AddressType1Enum::STREET)
    ->build();
```

