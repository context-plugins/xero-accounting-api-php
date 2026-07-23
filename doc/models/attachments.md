
# Attachments

## Structure

`Attachments`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `attachments` | [`?(Attachment[])`](../../doc/models/attachment.md) | Optional | - | getAttachments(): ?array | setAttachments(?array attachments): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\AttachmentsBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;

$attachments = AttachmentsBuilder::init()
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
    ->build();
```

