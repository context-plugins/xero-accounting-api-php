
# Employee

Find out more here: [http://developer.xero.com/documentation/api/employees/](http://developer.xero.com/documentation/api/employees/)

## Structure

`Employee`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `employeeID` | `?string` | Optional | The Xero identifier for an employee e.g. 297c2dc5-cc47-4afd-8ec8-74990b8761e9 | getEmployeeID(): ?string | setEmployeeID(?string employeeID): void |
| `externalLink` | [`?ExternalLink`](../../doc/models/external-link.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/) | getExternalLink(): ?ExternalLink | setExternalLink(?ExternalLink externalLink): void |
| `firstName` | `?string` | Optional | First name of an employee (max length = 255)<br><br>**Constraints**: *Maximum Length*: `255` | getFirstName(): ?string | setFirstName(?string firstName): void |
| `lastName` | `?string` | Optional | Last name of an employee (max length = 255)<br><br>**Constraints**: *Maximum Length*: `255` | getLastName(): ?string | setLastName(?string lastName): void |
| `status` | [`?string(Status10Enum)`](../../doc/models/status-10-enum.md) | Optional | Current status of an employee – see contact status types | getStatus(): ?string | setStatus(?string status): void |
| `statusAttributeString` | `?string` | Optional | A string to indicate if a invoice status | getStatusAttributeString(): ?string | setStatusAttributeString(?string statusAttributeString): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | - | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\EmployeeBuilder;
use XeroAccountingAPILib\Models\Builders\ExternalLinkBuilder;
use XeroAccountingAPILib\Models\LinkTypeEnum;
use XeroAccountingAPILib\Models\Status10Enum;

$employee = EmployeeBuilder::init()
    ->employeeID('000025ae-0000-0000-0000-000000000000')
    ->externalLink(
        ExternalLinkBuilder::init()
            ->description('Description8')
            ->linkType(LinkTypeEnum::TWITTER)
            ->url('Url4')
            ->build()
    )
    ->firstName('FirstName6')
    ->lastName('LastName6')
    ->status(Status10Enum::ACTIVE)
    ->statusAttributeString('ERROR')
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

