
# Contact Group

Find out more here: [http://developer.xero.com/documentation/api/contactgroups/](http://developer.xero.com/documentation/api/contactgroups/)

## Structure

`ContactGroup`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `contactGroupID` | `?string` | Optional | The Xero identifier for an contact group – specified as a string following the endpoint name. e.g. /297c2dc5-cc47-4afd-8ec8-74990b8761e9 | getContactGroupID(): ?string | setContactGroupID(?string contactGroupID): void |
| `contacts` | [`?(Contact[])`](../../doc/models/contact.md) | Optional | The ContactID and Name of Contacts in a contact group. Returned on GETs when the ContactGroupID is supplied in the URL. | getContacts(): ?array | setContacts(?array contacts): void |
| `name` | `?string` | Optional | The Name of the contact group. Required when creating a new contact  group | getName(): ?string | setName(?string name): void |
| `status` | [`?string(Status2Enum)`](../../doc/models/status-2-enum.md) | Optional | The Status of a contact group. To delete a contact group update the status to DELETED. Only contact groups with a status of ACTIVE are returned on GETs. | getStatus(): ?string | setStatus(?string status): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ContactGroupBuilder;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\Status2Enum;

$contactGroup = ContactGroupBuilder::init()
    ->contactGroupID('000001e2-0000-0000-0000-000000000000')
    ->contacts(
        [
            ContactBuilder::init()
                ->accountNumber('AccountNumber6')
                ->accountsPayableTaxType('AccountsPayableTaxType6')
                ->accountsReceivableTaxType('AccountsReceivableTaxType2')
                ->addresses(
                    [
                        AddressBuilder::init()
                            ->addressLine1('AddressLine14')
                            ->addressLine2('AddressLine20')
                            ->addressLine3('AddressLine38')
                            ->addressLine4('AddressLine46')
                            ->addressType(AddressTypeEnum::POBOX)
                            ->build()
                    ]
                )
                ->attachments(
                    [
                        AttachmentBuilder::init()
                            ->attachmentID('00000714-0000-0000-0000-000000000000')
                            ->contentLength(34)
                            ->fileName('FileName6')
                            ->includeOnline(false)
                            ->mimeType('MimeType6')
                            ->build(),
                        AttachmentBuilder::init()
                            ->attachmentID('00000714-0000-0000-0000-000000000000')
                            ->contentLength(34)
                            ->fileName('FileName6')
                            ->includeOnline(false)
                            ->mimeType('MimeType6')
                            ->build()
                    ]
                )
                ->build(),
            ContactBuilder::init()
                ->accountNumber('AccountNumber6')
                ->accountsPayableTaxType('AccountsPayableTaxType6')
                ->accountsReceivableTaxType('AccountsReceivableTaxType2')
                ->addresses(
                    [
                        AddressBuilder::init()
                            ->addressLine1('AddressLine14')
                            ->addressLine2('AddressLine20')
                            ->addressLine3('AddressLine38')
                            ->addressLine4('AddressLine46')
                            ->addressType(AddressTypeEnum::POBOX)
                            ->build()
                    ]
                )
                ->attachments(
                    [
                        AttachmentBuilder::init()
                            ->attachmentID('00000714-0000-0000-0000-000000000000')
                            ->contentLength(34)
                            ->fileName('FileName6')
                            ->includeOnline(false)
                            ->mimeType('MimeType6')
                            ->build(),
                        AttachmentBuilder::init()
                            ->attachmentID('00000714-0000-0000-0000-000000000000')
                            ->contentLength(34)
                            ->fileName('FileName6')
                            ->includeOnline(false)
                            ->mimeType('MimeType6')
                            ->build()
                    ]
                )
                ->build(),
            ContactBuilder::init()
                ->accountNumber('AccountNumber6')
                ->accountsPayableTaxType('AccountsPayableTaxType6')
                ->accountsReceivableTaxType('AccountsReceivableTaxType2')
                ->addresses(
                    [
                        AddressBuilder::init()
                            ->addressLine1('AddressLine14')
                            ->addressLine2('AddressLine20')
                            ->addressLine3('AddressLine38')
                            ->addressLine4('AddressLine46')
                            ->addressType(AddressTypeEnum::POBOX)
                            ->build()
                    ]
                )
                ->attachments(
                    [
                        AttachmentBuilder::init()
                            ->attachmentID('00000714-0000-0000-0000-000000000000')
                            ->contentLength(34)
                            ->fileName('FileName6')
                            ->includeOnline(false)
                            ->mimeType('MimeType6')
                            ->build(),
                        AttachmentBuilder::init()
                            ->attachmentID('00000714-0000-0000-0000-000000000000')
                            ->contentLength(34)
                            ->fileName('FileName6')
                            ->includeOnline(false)
                            ->mimeType('MimeType6')
                            ->build()
                    ]
                )
                ->build()
        ]
    )
    ->name('Name8')
    ->status(Status2Enum::ACTIVE)
    ->build();
```

