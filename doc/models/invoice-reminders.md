
# Invoice Reminders

## Structure

`InvoiceReminders`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `invoiceReminders` | [`?(InvoiceReminder[])`](../../doc/models/invoice-reminder.md) | Optional | - | getInvoiceReminders(): ?array | setInvoiceReminders(?array invoiceReminders): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\InvoiceRemindersBuilder;
use XeroAccountingAPILib\Models\Builders\InvoiceReminderBuilder;

$invoiceReminders = InvoiceRemindersBuilder::init()
    ->invoiceReminders(
        [
            InvoiceReminderBuilder::init()
                ->enabled(false)
                ->build(),
            InvoiceReminderBuilder::init()
                ->enabled(false)
                ->build(),
            InvoiceReminderBuilder::init()
                ->enabled(false)
                ->build()
        ]
    )
    ->build();
```

