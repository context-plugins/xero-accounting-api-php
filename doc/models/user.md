
# User

Find out more here: [http://developer.xero.com/documentation/api/users/](http://developer.xero.com/documentation/api/users/)

## Structure

`User`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `emailAddress` | `?string` | Optional | Email address of user | getEmailAddress(): ?string | setEmailAddress(?string emailAddress): void |
| `firstName` | `?string` | Optional | First name of user | getFirstName(): ?string | setFirstName(?string firstName): void |
| `isSubscriber` | `?bool` | Optional | Boolean to indicate if user is the subscriber | getIsSubscriber(): ?bool | setIsSubscriber(?bool isSubscriber): void |
| `lastName` | `?string` | Optional | Last name of user | getLastName(): ?string | setLastName(?string lastName): void |
| `organisationRole` | [`?string(OrganisationRoleEnum)`](../../doc/models/organisation-role-enum.md) | Optional | User role that defines permissions in Xero and via API (READONLY, INVOICEONLY, STANDARD, FINANCIALADVISER, etc) | getOrganisationRole(): ?string | setOrganisationRole(?string organisationRole): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | Timestamp of last change to user | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `userID` | `?string` | Optional | Xero identifier | getUserID(): ?string | setUserID(?string userID): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\UserBuilder;
use XeroAccountingAPILib\Models\OrganisationRoleEnum;

$user = UserBuilder::init()
    ->emailAddress('EmailAddress6')
    ->firstName('FirstName4')
    ->isSubscriber(false)
    ->lastName('LastName4')
    ->organisationRole(OrganisationRoleEnum::STANDARD)
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

