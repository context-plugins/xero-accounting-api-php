
# Overpayment

Find out more here: [http://developer.xero.com/documentation/api/overpayments/](http://developer.xero.com/documentation/api/overpayments/)

## Structure

`Overpayment`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `allocations` | [`?(Allocation[])`](../../doc/models/allocation.md) | Optional | See Allocations | getAllocations(): ?array | setAllocations(?array allocations): void |
| `appliedAmount` | `?float` | Optional | The amount of applied to an invoice | getAppliedAmount(): ?float | setAppliedAmount(?float appliedAmount): void |
| `attachments` | [`?(Attachment[])`](../../doc/models/attachment.md) | Optional | See Attachments | getAttachments(): ?array | setAttachments(?array attachments): void |
| `contact` | [`?Contact`](../../doc/models/contact.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/) | getContact(): ?Contact | setContact(?Contact contact): void |
| `currencyCode` | [`?string(CurrencyCodeEnum)`](../../doc/models/currency-code-enum.md) | Optional | 3 letter alpha code for the currency – see list of currency codes | getCurrencyCode(): ?string | setCurrencyCode(?string currencyCode): void |
| `currencyRate` | `?float` | Optional | The currency rate for a multicurrency overpayment. If no rate is specified, the XE.com day rate is used | getCurrencyRate(): ?float | setCurrencyRate(?float currencyRate): void |
| `date` | `?string` | Optional | The date the overpayment is created YYYY-MM-DD | getDate(): ?string | setDate(?string date): void |
| `hasAttachments` | `?bool` | Optional, Read-only | boolean to indicate if a overpayment has an attachment<br><br>**Default**: `false` | getHasAttachments(): ?bool | setHasAttachments(?bool hasAttachments): void |
| `lineAmountTypes` | [`?string(LineAmountTypesEnum)`](../../doc/models/line-amount-types-enum.md) | Optional | Line amounts are exclusive of tax by default if you don’t specify this element. See Line Amount Types | getLineAmountTypes(): ?string | setLineAmountTypes(?string lineAmountTypes): void |
| `lineItems` | [`?(LineItem[])`](../../doc/models/line-item.md) | Optional | See Overpayment Line Items | getLineItems(): ?array | setLineItems(?array lineItems): void |
| `overpaymentID` | `?string` | Optional | Xero generated unique identifier | getOverpaymentID(): ?string | setOverpaymentID(?string overpaymentID): void |
| `payments` | [`?(Payment[])`](../../doc/models/payment.md) | Optional | See Payments | getPayments(): ?array | setPayments(?array payments): void |
| `remainingCredit` | `?float` | Optional | The remaining credit balance on the overpayment | getRemainingCredit(): ?float | setRemainingCredit(?float remainingCredit): void |
| `status` | [`?string(Status3Enum)`](../../doc/models/status-3-enum.md) | Optional | See Overpayment Status Codes | getStatus(): ?string | setStatus(?string status): void |
| `subTotal` | `?float` | Optional | The subtotal of the overpayment excluding taxes | getSubTotal(): ?float | setSubTotal(?float subTotal): void |
| `total` | `?float` | Optional | The total of the overpayment (subtotal + total tax) | getTotal(): ?float | setTotal(?float total): void |
| `totalTax` | `?float` | Optional | The total tax on the overpayment | getTotalTax(): ?float | setTotalTax(?float totalTax): void |
| `type` | [`?string(Type1Enum)`](../../doc/models/type-1-enum.md) | Optional | See Overpayment Types | getType(): ?string | setType(?string type): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | UTC timestamp of last update to the overpayment | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\OverpaymentBuilder;
use XeroAccountingAPILib\Models\Builders\AllocationBuilder;
use XeroAccountingAPILib\Models\Builders\InvoiceBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;
use XeroAccountingAPILib\Models\Builders\ValidationErrorBuilder;
use XeroAccountingAPILib\Models\Builders\CreditNoteBuilder;
use XeroAccountingAPILib\Models\Builders\PrepaymentBuilder;

$overpayment = OverpaymentBuilder::init()
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
    ->currencyCode(CurrencyCodeEnum::GYD)
    ->hasAttachments(false)
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

