
# Credit Note

Find out more here: [http://developer.xero.com/documentation/api/credit-notes/](http://developer.xero.com/documentation/api/credit-notes/)

## Structure

`CreditNote`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `allocations` | [`?(Allocation[])`](../../doc/models/allocation.md) | Optional | See Allocations | getAllocations(): ?array | setAllocations(?array allocations): void |
| `appliedAmount` | `?float` | Optional | The amount of applied to an invoice | getAppliedAmount(): ?float | setAppliedAmount(?float appliedAmount): void |
| `brandingThemeID` | `?string` | Optional | See BrandingThemes | getBrandingThemeID(): ?string | setBrandingThemeID(?string brandingThemeID): void |
| `cISDeduction` | `?float` | Optional, Read-only | CIS deduction for UK contractors | getCISDeduction(): ?float | setCISDeduction(?float cISDeduction): void |
| `cISRate` | `?float` | Optional, Read-only | CIS Deduction rate for the organisation | getCISRate(): ?float | setCISRate(?float cISRate): void |
| `contact` | [`?Contact`](../../doc/models/contact.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/) | getContact(): ?Contact | setContact(?Contact contact): void |
| `creditNoteID` | `?string` | Optional | Xero generated unique identifier | getCreditNoteID(): ?string | setCreditNoteID(?string creditNoteID): void |
| `creditNoteNumber` | `?string` | Optional | ACCRECCREDIT – Unique alpha numeric code identifying credit note (when missing will auto-generate from your Organisation Invoice Settings) | getCreditNoteNumber(): ?string | setCreditNoteNumber(?string creditNoteNumber): void |
| `currencyCode` | [`?string(CurrencyCodeEnum)`](../../doc/models/currency-code-enum.md) | Optional | 3 letter alpha code for the currency – see list of currency codes | getCurrencyCode(): ?string | setCurrencyCode(?string currencyCode): void |
| `currencyRate` | `?float` | Optional | The currency rate for a multicurrency invoice. If no rate is specified, the XE.com day rate is used | getCurrencyRate(): ?float | setCurrencyRate(?float currencyRate): void |
| `date` | `?string` | Optional | The date the credit note is issued YYYY-MM-DD. If the Date element is not specified then it will default to the current date based on the timezone setting of the organisation | getDate(): ?string | setDate(?string date): void |
| `dueDate` | `?string` | Optional | Date invoice is due – YYYY-MM-DD | getDueDate(): ?string | setDueDate(?string dueDate): void |
| `fullyPaidOnDate` | `?string` | Optional | Date when credit note was fully paid(UTC format) | getFullyPaidOnDate(): ?string | setFullyPaidOnDate(?string fullyPaidOnDate): void |
| `hasAttachments` | `?bool` | Optional | boolean to indicate if a credit note has an attachment<br><br>**Default**: `false` | getHasAttachments(): ?bool | setHasAttachments(?bool hasAttachments): void |
| `hasErrors` | `?bool` | Optional | A boolean to indicate if a credit note has an validation errors<br><br>**Default**: `false` | getHasErrors(): ?bool | setHasErrors(?bool hasErrors): void |
| `lineAmountTypes` | [`?string(LineAmountTypesEnum)`](../../doc/models/line-amount-types-enum.md) | Optional | Line amounts are exclusive of tax by default if you don’t specify this element. See Line Amount Types | getLineAmountTypes(): ?string | setLineAmountTypes(?string lineAmountTypes): void |
| `lineItems` | [`?(LineItem[])`](../../doc/models/line-item.md) | Optional | See Invoice Line Items | getLineItems(): ?array | setLineItems(?array lineItems): void |
| `payments` | [`?(Payment[])`](../../doc/models/payment.md) | Optional | See Payments | getPayments(): ?array | setPayments(?array payments): void |
| `reference` | `?string` | Optional | ACCRECCREDIT only – additional reference number | getReference(): ?string | setReference(?string reference): void |
| `remainingCredit` | `?float` | Optional | The remaining credit balance on the Credit Note | getRemainingCredit(): ?float | setRemainingCredit(?float remainingCredit): void |
| `sentToContact` | `?bool` | Optional, Read-only | boolean to indicate if a credit note has been sent to a contact via  the Xero app (currently read only) | getSentToContact(): ?bool | setSentToContact(?bool sentToContact): void |
| `status` | [`?string(Status7Enum)`](../../doc/models/status-7-enum.md) | Optional | See Credit Note Status Codes | getStatus(): ?string | setStatus(?string status): void |
| `statusAttributeString` | `?string` | Optional | A string to indicate if a invoice status | getStatusAttributeString(): ?string | setStatusAttributeString(?string statusAttributeString): void |
| `subTotal` | `?float` | Optional | The subtotal of the credit note excluding taxes | getSubTotal(): ?float | setSubTotal(?float subTotal): void |
| `total` | `?float` | Optional | The total of the Credit Note(subtotal + total tax) | getTotal(): ?float | setTotal(?float total): void |
| `totalTax` | `?float` | Optional | The total tax on the credit note | getTotalTax(): ?float | setTotalTax(?float totalTax): void |
| `type` | [`?string(Type4Enum)`](../../doc/models/type-4-enum.md) | Optional | See Credit Note Types | getType(): ?string | setType(?string type): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | UTC timestamp of last update to the credit note | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |
| `warnings` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of warning messages from the API | getWarnings(): ?array | setWarnings(?array warnings): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\CreditNoteBuilder;
use XeroAccountingAPILib\Models\Builders\AllocationBuilder;
use XeroAccountingAPILib\Models\Builders\InvoiceBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;
use XeroAccountingAPILib\Models\Builders\ValidationErrorBuilder;
use XeroAccountingAPILib\Models\Builders\OverpaymentBuilder;
use XeroAccountingAPILib\Models\Builders\PrepaymentBuilder;

$creditNote = CreditNoteBuilder::init()
    ->allocations(
        [
            AllocationBuilder::init(
                2.44,
                'Date0',
                InvoiceBuilder::init()
                    ->amountCredited(89.1)
                    ->amountDue(153.52)
                    ->amountPaid(83.36)
                    ->attachments(
                        [
                            AttachmentBuilder::init()
                                ->attachmentID('00000714-0000-0000-0000-000000000000')
                                ->contentLength(34)
                                ->fileName('FileName6')
                                ->includeOnline(false)
                                ->mimeType('MimeType6')
                                ->build()
                        ]
                    )
                    ->brandingThemeID('00000b90-0000-0000-0000-000000000000')
                    ->build()
            )
                ->creditNote(
                    CreditNoteBuilder::init()
                        ->allocations(
                            [
                                AllocationBuilder::init(
                                    0.0,
                                    '',
                                    null
                                )->build(),
                                AllocationBuilder::init(
                                    0.0,
                                    '',
                                    null
                                )->build(),
                                AllocationBuilder::init(
                                    0.0,
                                    '',
                                    null
                                )->build()
                            ]
                        )
                        ->appliedAmount(212.18)
                        ->brandingThemeID('00000146-0000-0000-0000-000000000000')
                        ->cISDeduction(239.72)
                        ->cISRate(189)
                        ->build()
                )
                ->overpayment(
                    OverpaymentBuilder::init()
                        ->allocations(
                            [
                                AllocationBuilder::init(
                                    0.0,
                                    '',
                                    null
                                )->build(),
                                AllocationBuilder::init(
                                    0.0,
                                    '',
                                    null
                                )->build(),
                                AllocationBuilder::init(
                                    0.0,
                                    '',
                                    null
                                )->build()
                            ]
                        )
                        ->appliedAmount(99.9)
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
                        ->currencyCode(CurrencyCodeEnum::RWF)
                        ->build()
                )
                ->prepayment(
                    PrepaymentBuilder::init()
                        ->allocations(
                            [
                                AllocationBuilder::init(
                                    0.0,
                                    '',
                                    null
                                )->build()
                            ]
                        )
                        ->appliedAmount(126.26)
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
                        ->currencyCode(CurrencyCodeEnum::UYU)
                        ->build()
                )
                ->statusAttributeString('StatusAttributeString2')
                ->validationErrors(
                    [
                        ValidationErrorBuilder::init()
                            ->message('Message8')
                            ->build(),
                        ValidationErrorBuilder::init()
                            ->message('Message8')
                            ->build(),
                        ValidationErrorBuilder::init()
                            ->message('Message8')
                            ->build()
                    ]
                )
                ->build()
        ]
    )
    ->appliedAmount(2)
    ->brandingThemeID('000005e2-0000-0000-0000-000000000000')
    ->cISDeduction(251.52)
    ->cISRate(200.8)
    ->hasAttachments(false)
    ->hasErrors(false)
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

