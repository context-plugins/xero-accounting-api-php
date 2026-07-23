
# Linked Transaction

Find out more here: [http://developer.xero.com/documentation/api/linked-transactions/](http://developer.xero.com/documentation/api/linked-transactions/)

## Structure

`LinkedTransaction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `contactID` | `?string` | Optional | Filter by the combination of ContactID and Status. Get all the linked transactions that have been assigned to a particular customer and have a particular status e.g. GET /LinkedTransactions?ContactID=4bb34b03-3378-4bb2-a0ed-6345abf3224e&Status=APPROVED. | getContactID(): ?string | setContactID(?string contactID): void |
| `linkedTransactionID` | `?string` | Optional | The Xero identifier for an Linked Transaction e.g./LinkedTransactions/297c2dc5-cc47-4afd-8ec8-74990b8761e9 | getLinkedTransactionID(): ?string | setLinkedTransactionID(?string linkedTransactionID): void |
| `sourceLineItemID` | `?string` | Optional | The line item identifier from the source transaction. | getSourceLineItemID(): ?string | setSourceLineItemID(?string sourceLineItemID): void |
| `sourceTransactionID` | `?string` | Optional | Filter by the SourceTransactionID. Get all the linked transactions created from a particular ACCPAY invoice | getSourceTransactionID(): ?string | setSourceTransactionID(?string sourceTransactionID): void |
| `sourceTransactionTypeCode` | [`?string(SourceTransactionTypeCodeEnum)`](../../doc/models/source-transaction-type-code-enum.md) | Optional | The Type of the source tranasction. This will be ACCPAY if the linked transaction was created from an invoice and SPEND if it was created from a bank transaction. | getSourceTransactionTypeCode(): ?string | setSourceTransactionTypeCode(?string sourceTransactionTypeCode): void |
| `status` | [`?string(Status15Enum)`](../../doc/models/status-15-enum.md) | Optional | Filter by the combination of ContactID and Status. Get all the linked transactions that have been assigned to a particular customer and have a particular status e.g. GET /LinkedTransactions?ContactID=4bb34b03-3378-4bb2-a0ed-6345abf3224e&Status=APPROVED. | getStatus(): ?string | setStatus(?string status): void |
| `targetLineItemID` | `?string` | Optional | The line item identifier from the target transaction. It is possible  to link multiple billable expenses to the same TargetLineItemID. | getTargetLineItemID(): ?string | setTargetLineItemID(?string targetLineItemID): void |
| `targetTransactionID` | `?string` | Optional | Filter by the TargetTransactionID. Get all the linked transactions  allocated to a particular ACCREC invoice | getTargetTransactionID(): ?string | setTargetTransactionID(?string targetTransactionID): void |
| `type` | [`?string(Type7Enum)`](../../doc/models/type-7-enum.md) | Optional | This will always be BILLABLEEXPENSE. More types may be added in future. | getType(): ?string | setType(?string type): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | The last modified date in UTC format | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\LinkedTransactionBuilder;
use XeroAccountingAPILib\Models\SourceTransactionTypeCodeEnum;

$linkedTransaction = LinkedTransactionBuilder::init()
    ->contactID('00000962-0000-0000-0000-000000000000')
    ->linkedTransactionID('00000db0-0000-0000-0000-000000000000')
    ->sourceLineItemID('000012a8-0000-0000-0000-000000000000')
    ->sourceTransactionID('0000069e-0000-0000-0000-000000000000')
    ->sourceTransactionTypeCode(SourceTransactionTypeCodeEnum::ACCPAY)
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

