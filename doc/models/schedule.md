
# Schedule

Find out more here: [http://developer.xero.com/documentation/api/repeating-invoices/](http://developer.xero.com/documentation/api/repeating-invoices/)

## Structure

`Schedule`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dueDate` | `?int` | Optional | Integer used with due date type e.g 20 (of following month), 31 (of current month) | getDueDate(): ?int | setDueDate(?int dueDate): void |
| `dueDateType` | [`?string(DueDateTypeEnum)`](../../doc/models/due-date-type-enum.md) | Optional | the payment terms | getDueDateType(): ?string | setDueDateType(?string dueDateType): void |
| `endDate` | `?string` | Optional | Invoice end date – only returned if the template has an end date set | getEndDate(): ?string | setEndDate(?string endDate): void |
| `nextScheduledDate` | `?string` | Optional | The calendar date of the next invoice in the schedule to be generated | getNextScheduledDate(): ?string | setNextScheduledDate(?string nextScheduledDate): void |
| `period` | `?int` | Optional | Integer used with the unit e.g. 1 (every 1 week), 2 (every 2 months) | getPeriod(): ?int | setPeriod(?int period): void |
| `startDate` | `?string` | Optional | Date the first invoice of the current version of the repeating schedule was generated (changes when repeating invoice is edited) | getStartDate(): ?string | setStartDate(?string startDate): void |
| `unit` | [`?string(UnitEnum)`](../../doc/models/unit-enum.md) | Optional | One of the following - WEEKLY or MONTHLY | getUnit(): ?string | setUnit(?string unit): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ScheduleBuilder;
use XeroAccountingAPILib\Models\DueDateTypeEnum;

$schedule = ScheduleBuilder::init()
    ->dueDate(20)
    ->dueDateType(DueDateTypeEnum::DAYSAFTERINVOICEDATE)
    ->endDate('EndDate6')
    ->nextScheduledDate('NextScheduledDate4')
    ->period(64)
    ->build();
```

