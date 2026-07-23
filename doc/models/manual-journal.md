
# Manual Journal

Find out more here: [http://developer.xero.com/documentation/api/manual-journals/](http://developer.xero.com/documentation/api/manual-journals/)

## Structure

`ManualJournal`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `attachments` | [`?(Attachment[])`](../../doc/models/attachment.md) | Optional | Displays array of attachments from the API | getAttachments(): ?array | setAttachments(?array attachments): void |
| `date` | `?string` | Optional | Date journal was posted – YYYY-MM-DD | getDate(): ?string | setDate(?string date): void |
| `hasAttachments` | `?bool` | Optional, Read-only | Boolean to indicate if a manual journal has an attachment<br><br>**Default**: `false` | getHasAttachments(): ?bool | setHasAttachments(?bool hasAttachments): void |
| `journalLines` | [`?(ManualJournalLine[])`](../../doc/models/manual-journal-line.md) | Optional | See JournalLines | getJournalLines(): ?array | setJournalLines(?array journalLines): void |
| `lineAmountTypes` | [`?string(LineAmountTypesEnum)`](../../doc/models/line-amount-types-enum.md) | Optional | Line amounts are exclusive of tax by default if you don’t specify this element. See Line Amount Types | getLineAmountTypes(): ?string | setLineAmountTypes(?string lineAmountTypes): void |
| `manualJournalID` | `?string` | Optional | The Xero identifier for a Manual Journal | getManualJournalID(): ?string | setManualJournalID(?string manualJournalID): void |
| `narration` | `string` | Required | Description of journal being posted | getNarration(): string | setNarration(string narration): void |
| `showOnCashBasisReports` | `?bool` | Optional | Boolean – default is true if not specified | getShowOnCashBasisReports(): ?bool | setShowOnCashBasisReports(?bool showOnCashBasisReports): void |
| `status` | [`?string(Status16Enum)`](../../doc/models/status-16-enum.md) | Optional | See Manual Journal Status Codes | getStatus(): ?string | setStatus(?string status): void |
| `statusAttributeString` | `?string` | Optional | A string to indicate if a invoice status | getStatusAttributeString(): ?string | setStatusAttributeString(?string statusAttributeString): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | Last modified date UTC format | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `url` | `?string` | Optional | Url link to a source document – shown as “Go to [appName]” in the Xero app | getUrl(): ?string | setUrl(?string url): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |
| `warnings` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of warning messages from the API | getWarnings(): ?array | setWarnings(?array warnings): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ManualJournalBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\Builders\ManualJournalLineBuilder;
use XeroAccountingAPILib\Models\LineAmountTypesEnum;

$manualJournal = ManualJournalBuilder::init(
    'Narration2'
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
    ->date('Date2')
    ->hasAttachments(false)
    ->journalLines(
        [
            ManualJournalLineBuilder::init()
                ->accountCode('AccountCode2')
                ->accountID('000025e8-0000-0000-0000-000000000000')
                ->description('Description2')
                ->isBlank(false)
                ->lineAmount(127.64)
                ->build(),
            ManualJournalLineBuilder::init()
                ->accountCode('AccountCode2')
                ->accountID('000025e8-0000-0000-0000-000000000000')
                ->description('Description2')
                ->isBlank(false)
                ->lineAmount(127.64)
                ->build()
        ]
    )
    ->lineAmountTypes(LineAmountTypesEnum::EXCLUSIVE)
    ->statusAttributeString('ERROR')
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

