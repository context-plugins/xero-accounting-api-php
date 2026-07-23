
# Invoice Reminder

Find out more here: [http://developer.xero.com/documentation/api/invoice-reminders/](http://developer.xero.com/documentation/api/invoice-reminders/)

## Structure

`InvoiceReminder`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `enabled` | `?bool` | Optional | setting for on or off | getEnabled(): ?bool | setEnabled(?bool enabled): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\InvoiceReminderBuilder;

$invoiceReminder = InvoiceReminderBuilder::init()
    ->enabled(false)
    ->build();
```

