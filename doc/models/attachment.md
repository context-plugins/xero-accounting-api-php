
# Attachment

Find out more here: [http://developer.xero.com/documentation/api/attachments/](http://developer.xero.com/documentation/api/attachments/)

## Structure

`Attachment`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `attachmentID` | `?string` | Optional | Unique ID for the file | getAttachmentID(): ?string | setAttachmentID(?string attachmentID): void |
| `contentLength` | `?int` | Optional | Length of the file content | getContentLength(): ?int | setContentLength(?int contentLength): void |
| `fileName` | `?string` | Optional | Name of the file | getFileName(): ?string | setFileName(?string fileName): void |
| `includeOnline` | `?bool` | Optional | Include the file with the online invoice | getIncludeOnline(): ?bool | setIncludeOnline(?bool includeOnline): void |
| `mimeType` | `?string` | Optional | Type of file | getMimeType(): ?string | setMimeType(?string mimeType): void |
| `url` | `?string` | Optional | URL to the file on xero.com | getUrl(): ?string | setUrl(?string url): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;

$attachment = AttachmentBuilder::init()
    ->attachmentID('00000000-0000-0000-0000-000000000000')
    ->contentLength(174)
    ->fileName('xero-dev.jpg')
    ->includeOnline(false)
    ->mimeType('image/jpg')
    ->url('https://api.xero.com/api.xro/2.0/Accounts/da962997-a8bd-4dff-9616-01cdc199283f/Attachments/sample5.jpg')
    ->build();
```

