
# Receipts

## Structure

`Receipts`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `receipts` | [`?(Receipt[])`](../../doc/models/receipt.md) | Optional | - | getReceipts(): ?array | setReceipts(?array receipts): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ReceiptsBuilder;
use XeroAccountingAPILib\Models\Builders\ReceiptBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\LineAmountTypesEnum;

$receipts = ReceiptsBuilder::init()
    ->receipts(
        [
            ReceiptBuilder::init()
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
                ->lineAmountTypes(LineAmountTypesEnum::NOTAX)
                ->build(),
            ReceiptBuilder::init()
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
                ->lineAmountTypes(LineAmountTypesEnum::NOTAX)
                ->build(),
            ReceiptBuilder::init()
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
                ->lineAmountTypes(LineAmountTypesEnum::NOTAX)
                ->build()
        ]
    )
    ->build();
```

