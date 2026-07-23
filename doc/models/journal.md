
# Journal

Find out more here: [http://developer.xero.com/documentation/api/journals/](http://developer.xero.com/documentation/api/journals/)

## Structure

`Journal`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `createdDateUTC` | `?string` | Optional, Read-only | Created date UTC format | getCreatedDateUTC(): ?string | setCreatedDateUTC(?string createdDateUTC): void |
| `journalDate` | `?string` | Optional | Date the journal was posted | getJournalDate(): ?string | setJournalDate(?string journalDate): void |
| `journalID` | `?string` | Optional | Xero identifier | getJournalID(): ?string | setJournalID(?string journalID): void |
| `journalLines` | [`?(JournalLine[])`](../../doc/models/journal-line.md) | Optional | See JournalLines | getJournalLines(): ?array | setJournalLines(?array journalLines): void |
| `journalNumber` | `?int` | Optional | Xero generated journal number | getJournalNumber(): ?int | setJournalNumber(?int journalNumber): void |
| `reference` | `?string` | Optional | reference field for additional indetifying information | getReference(): ?string | setReference(?string reference): void |
| `sourceID` | `?string` | Optional | The identifier for the source transaction (e.g. InvoiceID) | getSourceID(): ?string | setSourceID(?string sourceID): void |
| `sourceType` | [`?string(SourceTypeEnum)`](../../doc/models/source-type-enum.md) | Optional | The journal source type. The type of transaction that created the journal | getSourceType(): ?string | setSourceType(?string sourceType): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\JournalBuilder;
use XeroAccountingAPILib\Models\Builders\JournalLineBuilder;
use XeroAccountingAPILib\Models\AccountTypeEnum;

$journal = JournalBuilder::init()
    ->createdDateUTC('/Date(1573755038314)/')
    ->journalDate('JournalDate6')
    ->journalID('000021ec-0000-0000-0000-000000000000')
    ->journalLines(
        [
            JournalLineBuilder::init()
                ->accountCode('AccountCode2')
                ->accountID('000025e8-0000-0000-0000-000000000000')
                ->accountName('AccountName8')
                ->accountType(AccountTypeEnum::EXPENSE)
                ->description('Description2')
                ->build(),
            JournalLineBuilder::init()
                ->accountCode('AccountCode2')
                ->accountID('000025e8-0000-0000-0000-000000000000')
                ->accountName('AccountName8')
                ->accountType(AccountTypeEnum::EXPENSE)
                ->description('Description2')
                ->build(),
            JournalLineBuilder::init()
                ->accountCode('AccountCode2')
                ->accountID('000025e8-0000-0000-0000-000000000000')
                ->accountName('AccountName8')
                ->accountType(AccountTypeEnum::EXPENSE)
                ->description('Description2')
                ->build()
        ]
    )
    ->journalNumber(90)
    ->build();
```

