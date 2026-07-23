
# Ten Ninety Nine Contact

## Structure

`TenNinetyNineContact`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `box1` | `?float` | Optional | Box 1 on 1099 Form | getBox1(): ?float | setBox1(?float box1): void |
| `box10` | `?float` | Optional | Box 10 on 1099 Form | getBox10(): ?float | setBox10(?float box10): void |
| `box11` | `?float` | Optional | Box 11 on 1099 Form | getBox11(): ?float | setBox11(?float box11): void |
| `box13` | `?float` | Optional | Box 13 on 1099 Form | getBox13(): ?float | setBox13(?float box13): void |
| `box14` | `?float` | Optional | Box 14 on 1099 Form | getBox14(): ?float | setBox14(?float box14): void |
| `box2` | `?float` | Optional | Box 2 on 1099 Form | getBox2(): ?float | setBox2(?float box2): void |
| `box3` | `?float` | Optional | Box 3 on 1099 Form | getBox3(): ?float | setBox3(?float box3): void |
| `box4` | `?float` | Optional | Box 4 on 1099 Form | getBox4(): ?float | setBox4(?float box4): void |
| `box5` | `?float` | Optional | Box 5 on 1099 Form | getBox5(): ?float | setBox5(?float box5): void |
| `box6` | `?float` | Optional | Box 6 on 1099 Form | getBox6(): ?float | setBox6(?float box6): void |
| `box7` | `?float` | Optional | Box 7 on 1099 Form | getBox7(): ?float | setBox7(?float box7): void |
| `box8` | `?float` | Optional | Box 8 on 1099 Form | getBox8(): ?float | setBox8(?float box8): void |
| `box9` | `?float` | Optional | Box 9 on 1099 Form | getBox9(): ?float | setBox9(?float box9): void |
| `city` | `?string` | Optional | Contact city on 1099 Form | getCity(): ?string | setCity(?string city): void |
| `contactId` | `?string` | Optional | Contact contact id | getContactId(): ?string | setContactId(?string contactId): void |
| `email` | `?string` | Optional | Contact email on 1099 Form | getEmail(): ?string | setEmail(?string email): void |
| `federalTaxIDType` | `?string` | Optional | Contact Fed Tax ID type | getFederalTaxIDType(): ?string | setFederalTaxIDType(?string federalTaxIDType): void |
| `name` | `?string` | Optional | Contact name on 1099 Form | getName(): ?string | setName(?string name): void |
| `state` | `?string` | Optional | Contact State on 1099 Form | getState(): ?string | setState(?string state): void |
| `streetAddress` | `?string` | Optional | Contact address on 1099 Form | getStreetAddress(): ?string | setStreetAddress(?string streetAddress): void |
| `taxID` | `?string` | Optional | Contact tax id on 1099 Form | getTaxID(): ?string | setTaxID(?string taxID): void |
| `zip` | `?string` | Optional | Contact zip on 1099 Form | getZip(): ?string | setZip(?string zip): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\TenNinetyNineContactBuilder;

$tenNinetyNineContact = TenNinetyNineContactBuilder::init()
    ->box1(48.26)
    ->box10(92.98)
    ->box11(212.66)
    ->box13(217.28)
    ->box14(141.32)
    ->build();
```

