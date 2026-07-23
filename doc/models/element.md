
# Element

Find out more here: [https://developer.xero.com/documentation/api/http-response-codes](https://developer.xero.com/documentation/api/http-response-codes)

## Structure

`Element`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `bankTransactionID` | `?string` | Optional | - | getBankTransactionID(): ?string | setBankTransactionID(?string bankTransactionID): void |
| `batchPaymentID` | `?string` | Optional | Unique ID for batch payment object with validation error | getBatchPaymentID(): ?string | setBatchPaymentID(?string batchPaymentID): void |
| `contactID` | `?string` | Optional | - | getContactID(): ?string | setContactID(?string contactID): void |
| `creditNoteID` | `?string` | Optional | - | getCreditNoteID(): ?string | setCreditNoteID(?string creditNoteID): void |
| `invoiceID` | `?string` | Optional | - | getInvoiceID(): ?string | setInvoiceID(?string invoiceID): void |
| `itemID` | `?string` | Optional | - | getItemID(): ?string | setItemID(?string itemID): void |
| `purchaseOrderID` | `?string` | Optional | - | getPurchaseOrderID(): ?string | setPurchaseOrderID(?string purchaseOrderID): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Array of Validation Error message | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ElementBuilder;

$element = ElementBuilder::init()
    ->bankTransactionID('0000218e-0000-0000-0000-000000000000')
    ->batchPaymentID('00001a4a-0000-0000-0000-000000000000')
    ->contactID('00002310-0000-0000-0000-000000000000')
    ->creditNoteID('00000acc-0000-0000-0000-000000000000')
    ->invoiceID('00001354-0000-0000-0000-000000000000')
    ->build();
```

