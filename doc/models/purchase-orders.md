
# Purchase Orders

## Structure

`PurchaseOrders`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `purchaseOrders` | [`?(PurchaseOrder[])`](../../doc/models/purchase-order.md) | Optional | - | getPurchaseOrders(): ?array | setPurchaseOrders(?array purchaseOrders): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\PurchaseOrdersBuilder;
use XeroAccountingAPILib\Models\Builders\PurchaseOrderBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;

$purchaseOrders = PurchaseOrdersBuilder::init()
    ->purchaseOrders(
        [
            PurchaseOrderBuilder::init()
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
                ->attentionTo('AttentionTo4')
                ->brandingThemeID('00000d68-0000-0000-0000-000000000000')
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
                ->currencyCode(CurrencyCodeEnum::TZS)
                ->build(),
            PurchaseOrderBuilder::init()
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
                ->attentionTo('AttentionTo4')
                ->brandingThemeID('00000d68-0000-0000-0000-000000000000')
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
                ->currencyCode(CurrencyCodeEnum::TZS)
                ->build(),
            PurchaseOrderBuilder::init()
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
                ->attentionTo('AttentionTo4')
                ->brandingThemeID('00000d68-0000-0000-0000-000000000000')
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
                ->currencyCode(CurrencyCodeEnum::TZS)
                ->build()
        ]
    )
    ->build();
```

