
# Contact Person

Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/)

## Structure

`ContactPerson`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `emailAddress` | `?string` | Optional | Email address of person | getEmailAddress(): ?string | setEmailAddress(?string emailAddress): void |
| `firstName` | `?string` | Optional | First name of person | getFirstName(): ?string | setFirstName(?string firstName): void |
| `includeInEmails` | `?bool` | Optional | boolean to indicate whether contact should be included on emails with invoices etc. | getIncludeInEmails(): ?bool | setIncludeInEmails(?bool includeInEmails): void |
| `lastName` | `?string` | Optional | Last name of person | getLastName(): ?string | setLastName(?string lastName): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ContactPersonBuilder;

$contactPerson = ContactPersonBuilder::init()
    ->emailAddress('EmailAddress6')
    ->firstName('FirstName4')
    ->includeInEmails(false)
    ->lastName('LastName4')
    ->build();
```

