
# Journals

## Structure

`Journals`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `journals` | [`?(Journal[])`](../../doc/models/journal.md) | Optional | - | getJournals(): ?array | setJournals(?array journals): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\JournalsBuilder;
use XeroAccountingAPILib\Models\Builders\JournalBuilder;
use XeroAccountingAPILib\Models\Builders\JournalLineBuilder;
use XeroAccountingAPILib\Models\AccountTypeEnum;

$journals = JournalsBuilder::init()
    ->journals(
        [
            JournalBuilder::init()
                ->createdDateUTC('CreatedDateUTC6')
                ->journalDate('JournalDate6')
                ->journalID('00002578-0000-0000-0000-000000000000')
                ->journalLines(
                    [
                        JournalLineBuilder::init()
                            ->accountCode('AccountCode2')
                            ->accountID('000025e8-0000-0000-0000-000000000000')
                            ->accountName('AccountName8')
                            ->accountType(AccountTypeEnum::EXPENSE)
                            ->description('Description2')
                            ->build()
                    ]
                )
                ->journalNumber(166)
                ->build(),
            JournalBuilder::init()
                ->createdDateUTC('CreatedDateUTC6')
                ->journalDate('JournalDate6')
                ->journalID('00002578-0000-0000-0000-000000000000')
                ->journalLines(
                    [
                        JournalLineBuilder::init()
                            ->accountCode('AccountCode2')
                            ->accountID('000025e8-0000-0000-0000-000000000000')
                            ->accountName('AccountName8')
                            ->accountType(AccountTypeEnum::EXPENSE)
                            ->description('Description2')
                            ->build()
                    ]
                )
                ->journalNumber(166)
                ->build(),
            JournalBuilder::init()
                ->createdDateUTC('CreatedDateUTC6')
                ->journalDate('JournalDate6')
                ->journalID('00002578-0000-0000-0000-000000000000')
                ->journalLines(
                    [
                        JournalLineBuilder::init()
                            ->accountCode('AccountCode2')
                            ->accountID('000025e8-0000-0000-0000-000000000000')
                            ->accountName('AccountName8')
                            ->accountType(AccountTypeEnum::EXPENSE)
                            ->description('Description2')
                            ->build()
                    ]
                )
                ->journalNumber(166)
                ->build()
        ]
    )
    ->build();
```

