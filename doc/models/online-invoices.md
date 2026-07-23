
# Online Invoices

## Structure

`OnlineInvoices`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `onlineInvoices` | [`?(OnlineInvoice[])`](../../doc/models/online-invoice.md) | Optional | - | getOnlineInvoices(): ?array | setOnlineInvoices(?array onlineInvoices): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\OnlineInvoicesBuilder;
use XeroAccountingAPILib\Models\Builders\OnlineInvoiceBuilder;

$onlineInvoices = OnlineInvoicesBuilder::init()
    ->onlineInvoices(
        [
            OnlineInvoiceBuilder::init()
                ->onlineInvoiceUrl('OnlineInvoiceUrl0')
                ->build(),
            OnlineInvoiceBuilder::init()
                ->onlineInvoiceUrl('OnlineInvoiceUrl0')
                ->build(),
            OnlineInvoiceBuilder::init()
                ->onlineInvoiceUrl('OnlineInvoiceUrl0')
                ->build()
        ]
    )
    ->build();
```

