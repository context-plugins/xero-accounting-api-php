
# History Records

## Structure

`HistoryRecords`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `historyRecords` | [`?(HistoryRecord[])`](../../doc/models/history-record.md) | Optional | - | getHistoryRecords(): ?array | setHistoryRecords(?array historyRecords): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\HistoryRecordsBuilder;
use XeroAccountingAPILib\Models\Builders\HistoryRecordBuilder;

$historyRecords = HistoryRecordsBuilder::init()
    ->historyRecords(
        [
            HistoryRecordBuilder::init()
                ->changes('Changes6')
                ->dateUTC('DateUTC8')
                ->details('Details4')
                ->user('User2')
                ->build(),
            HistoryRecordBuilder::init()
                ->changes('Changes6')
                ->dateUTC('DateUTC8')
                ->details('Details4')
                ->user('User2')
                ->build(),
            HistoryRecordBuilder::init()
                ->changes('Changes6')
                ->dateUTC('DateUTC8')
                ->details('Details4')
                ->user('User2')
                ->build()
        ]
    )
    ->build();
```

