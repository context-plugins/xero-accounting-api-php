
# Online Invoice

Find out more here: [http://developer.xero.com/documentation/api/invoices/](http://developer.xero.com/documentation/api/invoices/)

## Structure

`OnlineInvoice`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `onlineInvoiceUrl` | `?string` | Optional | the URL to an online invoice | getOnlineInvoiceUrl(): ?string | setOnlineInvoiceUrl(?string onlineInvoiceUrl): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\OnlineInvoiceBuilder;

$onlineInvoice = OnlineInvoiceBuilder::init()
    ->onlineInvoiceUrl('OnlineInvoiceUrl2')
    ->build();
```

