
# Receipt

Find out more here: [http://developer.xero.com/documentation/api/receipts/](http://developer.xero.com/documentation/api/receipts/)

## Structure

`Receipt`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `attachments` | [`?(Attachment[])`](../../doc/models/attachment.md) | Optional | Displays array of attachments from the API | getAttachments(): ?array | setAttachments(?array attachments): void |
| `contact` | [`?Contact`](../../doc/models/contact.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/) | getContact(): ?Contact | setContact(?Contact contact): void |
| `date` | `?string` | Optional | Date of receipt – YYYY-MM-DD | getDate(): ?string | setDate(?string date): void |
| `hasAttachments` | `?bool` | Optional, Read-only | boolean to indicate if a receipt has an attachment<br><br>**Default**: `false` | getHasAttachments(): ?bool | setHasAttachments(?bool hasAttachments): void |
| `lineAmountTypes` | [`?string(LineAmountTypesEnum)`](../../doc/models/line-amount-types-enum.md) | Optional | Line amounts are exclusive of tax by default if you don’t specify this element. See Line Amount Types | getLineAmountTypes(): ?string | setLineAmountTypes(?string lineAmountTypes): void |
| `lineItems` | [`?(LineItem[])`](../../doc/models/line-item.md) | Optional | - | getLineItems(): ?array | setLineItems(?array lineItems): void |
| `receiptID` | `?string` | Optional | Xero generated unique identifier for receipt | getReceiptID(): ?string | setReceiptID(?string receiptID): void |
| `receiptNumber` | `?string` | Optional, Read-only | Xero generated sequence number for receipt in current claim for a given user | getReceiptNumber(): ?string | setReceiptNumber(?string receiptNumber): void |
| `reference` | `?string` | Optional | Additional reference number | getReference(): ?string | setReference(?string reference): void |
| `status` | [`?string(Status11Enum)`](../../doc/models/status-11-enum.md) | Optional | Current status of receipt – see status types | getStatus(): ?string | setStatus(?string status): void |
| `subTotal` | `?float` | Optional | Total of receipt excluding taxes | getSubTotal(): ?float | setSubTotal(?float subTotal): void |
| `total` | `?float` | Optional | Total of receipt tax inclusive (i.e. SubTotal + TotalTax) | getTotal(): ?float | setTotal(?float total): void |
| `totalTax` | `?float` | Optional | Total tax on receipt | getTotalTax(): ?float | setTotalTax(?float totalTax): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | Last modified date UTC format | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `url` | `?string` | Optional, Read-only | URL link to a source document – shown as “Go to [appName]” in the Xero app | getUrl(): ?string | setUrl(?string url): void |
| `user` | [`?User`](../../doc/models/user.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/users/](http://developer.xero.com/documentation/api/users/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/users/](http://developer.xero.com/documentation/api/users/) | getUser(): ?User | setUser(?User user): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |
| `warnings` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of warning messages from the API | getWarnings(): ?array | setWarnings(?array warnings): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ReceiptBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\LineAmountTypesEnum;

$receipt = ReceiptBuilder::init()
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
    ->contact(
        ContactBuilder::init()
            ->accountNumber('AccountNumber2')
            ->accountsPayableTaxType('AccountsPayableTaxType2')
            ->accountsReceivableTaxType('AccountsReceivableTaxType6')
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
    )
    ->date('Date2')
    ->hasAttachments(false)
    ->lineAmountTypes(LineAmountTypesEnum::EXCLUSIVE)
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

