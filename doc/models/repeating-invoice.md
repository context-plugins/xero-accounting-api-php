
# Repeating Invoice

Find out more here: [http://developer.xero.com/documentation/api/repeating-invoices/](http://developer.xero.com/documentation/api/repeating-invoices/)

## Structure

`RepeatingInvoice`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `attachments` | [`?(Attachment[])`](../../doc/models/attachment.md) | Optional | Displays array of attachments from the API | getAttachments(): ?array | setAttachments(?array attachments): void |
| `brandingThemeID` | `?string` | Optional | See BrandingThemes | getBrandingThemeID(): ?string | setBrandingThemeID(?string brandingThemeID): void |
| `contact` | [`?Contact`](../../doc/models/contact.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/) | getContact(): ?Contact | setContact(?Contact contact): void |
| `currencyCode` | [`?string(CurrencyCodeEnum)`](../../doc/models/currency-code-enum.md) | Optional | 3 letter alpha code for the currency – see list of currency codes | getCurrencyCode(): ?string | setCurrencyCode(?string currencyCode): void |
| `hasAttachments` | `?bool` | Optional, Read-only | boolean to indicate if an invoice has an attachment<br><br>**Default**: `false` | getHasAttachments(): ?bool | setHasAttachments(?bool hasAttachments): void |
| `iD` | `?string` | Optional | Xero generated unique identifier for repeating invoice template | getID(): ?string | setID(?string iD): void |
| `lineAmountTypes` | [`?string(LineAmountTypesEnum)`](../../doc/models/line-amount-types-enum.md) | Optional | Line amounts are exclusive of tax by default if you don’t specify this element. See Line Amount Types | getLineAmountTypes(): ?string | setLineAmountTypes(?string lineAmountTypes): void |
| `lineItems` | [`?(LineItem[])`](../../doc/models/line-item.md) | Optional | See LineItems | getLineItems(): ?array | setLineItems(?array lineItems): void |
| `reference` | `?string` | Optional | ACCREC only – additional reference number | getReference(): ?string | setReference(?string reference): void |
| `repeatingInvoiceID` | `?string` | Optional | Xero generated unique identifier for repeating invoice template | getRepeatingInvoiceID(): ?string | setRepeatingInvoiceID(?string repeatingInvoiceID): void |
| `schedule` | [`?Schedule`](../../doc/models/schedule.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/repeating-invoices/](http://developer.xero.com/documentation/api/repeating-invoices/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/repeating-invoices/](http://developer.xero.com/documentation/api/repeating-invoices/) | getSchedule(): ?Schedule | setSchedule(?Schedule schedule): void |
| `status` | [`?string(Status18Enum)`](../../doc/models/status-18-enum.md) | Optional | One of the following - DRAFT or AUTHORISED – See Invoice Status Codes | getStatus(): ?string | setStatus(?string status): void |
| `subTotal` | `?float` | Optional | Total of invoice excluding taxes | getSubTotal(): ?float | setSubTotal(?float subTotal): void |
| `total` | `?float` | Optional | Total of Invoice tax inclusive (i.e. SubTotal + TotalTax) | getTotal(): ?float | setTotal(?float total): void |
| `totalTax` | `?float` | Optional | Total tax on invoice | getTotalTax(): ?float | setTotalTax(?float totalTax): void |
| `type` | [`?string(Type8Enum)`](../../doc/models/type-8-enum.md) | Optional | See Invoice Types | getType(): ?string | setType(?string type): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\RepeatingInvoiceBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;

$repeatingInvoice = RepeatingInvoiceBuilder::init()
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
    ->brandingThemeID('00001772-0000-0000-0000-000000000000')
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
    ->currencyCode(CurrencyCodeEnum::UZS)
    ->hasAttachments(false)
    ->build();
```

