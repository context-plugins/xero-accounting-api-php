
# Contacts

## Structure

`Contacts`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `contacts` | [`?(Contact[])`](../../doc/models/contact.md) | Optional | - | getContacts(): ?array | setContacts(?array contacts): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ContactsBuilder;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;

$contacts = ContactsBuilder::init()
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
                ->build()
        ]
    )
    ->build();
```

