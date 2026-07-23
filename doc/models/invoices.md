
# Invoices

## Structure

`Invoices`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `invoices` | [`?(Invoice[])`](../../doc/models/invoice.md) | Optional | - | getInvoices(): ?array | setInvoices(?array invoices): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\InvoicesBuilder;
use XeroAccountingAPILib\Models\Builders\InvoiceBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;

$invoices = InvoicesBuilder::init()
    ->invoices(
        [
            InvoiceBuilder::init()
                ->amountCredited(149.22)
                ->amountDue(213.64)
                ->amountPaid(143.48)
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
                ->brandingThemeID('000008b4-0000-0000-0000-000000000000')
                ->build()
        ]
    )
    ->build();
```

