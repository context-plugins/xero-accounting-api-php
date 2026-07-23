
# History Record

Find out more here: [https://developer.xero.com/documentation/api/history-and-notes](https://developer.xero.com/documentation/api/history-and-notes)

## Structure

`HistoryRecord`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `changes` | `?string` | Optional | Name of branding theme | getChanges(): ?string | setChanges(?string changes): void |
| `dateUTC` | `?string` | Optional, Read-only | UTC timestamp of creation date of branding theme | getDateUTC(): ?string | setDateUTC(?string dateUTC): void |
| `details` | `?string` | Optional | details | getDetails(): ?string | setDetails(?string details): void |
| `user` | `?string` | Optional | has a value of 0 | getUser(): ?string | setUser(?string user): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\HistoryRecordBuilder;

$historyRecord = HistoryRecordBuilder::init()
    ->changes('Changes6')
    ->dateUTC('/Date(1573755038314)/')
    ->details('Details4')
    ->user('User2')
    ->build();
```

