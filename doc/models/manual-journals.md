
# Manual Journals

## Structure

`ManualJournals`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `manualJournals` | [`?(ManualJournal[])`](../../doc/models/manual-journal.md) | Optional | - | getManualJournals(): ?array | setManualJournals(?array manualJournals): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ManualJournalsBuilder;
use XeroAccountingAPILib\Models\Builders\ManualJournalBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\Builders\ManualJournalLineBuilder;
use XeroAccountingAPILib\Models\LineAmountTypesEnum;

$manualJournals = ManualJournalsBuilder::init()
    ->manualJournals(
        [
            ManualJournalBuilder::init(
                'Narration6'
            )
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
                ->date('Date6')
                ->hasAttachments(false)
                ->journalLines(
                    [
                        ManualJournalLineBuilder::init()
                            ->accountCode('AccountCode2')
                            ->accountID('000025e8-0000-0000-0000-000000000000')
                            ->description('Description2')
                            ->isBlank(false)
                            ->lineAmount(127.64)
                            ->build()
                    ]
                )
                ->lineAmountTypes(LineAmountTypesEnum::NOTAX)
                ->build(),
            ManualJournalBuilder::init(
                'Narration6'
            )
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
                ->date('Date6')
                ->hasAttachments(false)
                ->journalLines(
                    [
                        ManualJournalLineBuilder::init()
                            ->accountCode('AccountCode2')
                            ->accountID('000025e8-0000-0000-0000-000000000000')
                            ->description('Description2')
                            ->isBlank(false)
                            ->lineAmount(127.64)
                            ->build()
                    ]
                )
                ->lineAmountTypes(LineAmountTypesEnum::NOTAX)
                ->build()
        ]
    )
    ->build();
```

