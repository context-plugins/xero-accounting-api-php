
# Repeating Invoices

## Structure

`RepeatingInvoices`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `repeatingInvoices` | [`?(RepeatingInvoice[])`](../../doc/models/repeating-invoice.md) | Optional | - | getRepeatingInvoices(): ?array | setRepeatingInvoices(?array repeatingInvoices): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\RepeatingInvoicesBuilder;
use XeroAccountingAPILib\Models\Builders\RepeatingInvoiceBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;

$repeatingInvoices = RepeatingInvoicesBuilder::init()
    ->repeatingInvoices(
        [
            RepeatingInvoiceBuilder::init()
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
                ->brandingThemeID('00001f00-0000-0000-0000-000000000000')
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
                ->currencyCode(CurrencyCodeEnum::NIO)
                ->hasAttachments(false)
                ->build(),
            RepeatingInvoiceBuilder::init()
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
                ->brandingThemeID('00001f00-0000-0000-0000-000000000000')
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
                ->currencyCode(CurrencyCodeEnum::NIO)
                ->hasAttachments(false)
                ->build(),
            RepeatingInvoiceBuilder::init()
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
                ->brandingThemeID('00001f00-0000-0000-0000-000000000000')
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
                ->currencyCode(CurrencyCodeEnum::NIO)
                ->hasAttachments(false)
                ->build()
        ]
    )
    ->build();
```

