
# Payment

Find out more here: [http://developer.xero.com/documentation/api/payments/](http://developer.xero.com/documentation/api/payments/)

## Structure

`Payment`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `account` | [`?Account`](../../doc/models/account.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/accounts/](http://developer.xero.com/documentation/api/accounts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/accounts/](http://developer.xero.com/documentation/api/accounts/) | getAccount(): ?Account | setAccount(?Account account): void |
| `amount` | `?float` | Optional | The amount of the payment. Must be less than or equal to the outstanding amount owing on the invoice e.g. 200.00 | getAmount(): ?float | setAmount(?float amount): void |
| `bankAccountNumber` | `?string` | Optional | The suppliers bank account number the payment is being made to | getBankAccountNumber(): ?string | setBankAccountNumber(?string bankAccountNumber): void |
| `batchPaymentID` | `?string` | Optional | Present if the payment was created as part of a batch. | getBatchPaymentID(): ?string | setBatchPaymentID(?string batchPaymentID): void |
| `code` | `?string` | Optional | Code of account you are using to make the payment e.g. 001 (note- not all accounts have a code value) | getCode(): ?string | setCode(?string code): void |
| `creditNote` | [`?CreditNote`](../../doc/models/credit-note.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/credit-notes/](http://developer.xero.com/documentation/api/credit-notes/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/credit-notes/](http://developer.xero.com/documentation/api/credit-notes/) | getCreditNote(): ?CreditNote | setCreditNote(?CreditNote creditNote): void |
| `creditNoteNumber` | `?string` | Optional | Number of invoice or credit note you are applying payment to e.g. INV-4003 | getCreditNoteNumber(): ?string | setCreditNoteNumber(?string creditNoteNumber): void |
| `currencyRate` | `?float` | Optional | Exchange rate when payment is received. Only used for non base currency invoices and credit notes e.g. 0.7500 | getCurrencyRate(): ?float | setCurrencyRate(?float currencyRate): void |
| `date` | `?string` | Optional | Date the payment is being made (YYYY-MM-DD) e.g. 2009-09-06 | getDate(): ?string | setDate(?string date): void |
| `details` | `?string` | Optional | The information to appear on the supplier's bank account | getDetails(): ?string | setDetails(?string details): void |
| `hasAccount` | `?bool` | Optional | A boolean to indicate if a contact has an validation errors<br><br>**Default**: `false` | getHasAccount(): ?bool | setHasAccount(?bool hasAccount): void |
| `hasValidationErrors` | `?bool` | Optional | A boolean to indicate if a contact has an validation errors<br><br>**Default**: `false` | getHasValidationErrors(): ?bool | setHasValidationErrors(?bool hasValidationErrors): void |
| `invoice` | [`?Invoice`](../../doc/models/invoice.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/invoices/](http://developer.xero.com/documentation/api/invoices/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/invoices/](http://developer.xero.com/documentation/api/invoices/) | getInvoice(): ?Invoice | setInvoice(?Invoice invoice): void |
| `invoiceNumber` | `?string` | Optional | Number of invoice or credit note you are applying payment to e.g.INV-4003 | getInvoiceNumber(): ?string | setInvoiceNumber(?string invoiceNumber): void |
| `isReconciled` | `?bool` | Optional | An optional parameter for the payment. A boolean indicating whether you would like the payment to be created as reconciled when using PUT, or whether a payment has been reconciled when using GET | getIsReconciled(): ?bool | setIsReconciled(?bool isReconciled): void |
| `overpayment` | [`?Overpayment`](../../doc/models/overpayment.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/overpayments/](http://developer.xero.com/documentation/api/overpayments/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/overpayments/](http://developer.xero.com/documentation/api/overpayments/) | getOverpayment(): ?Overpayment | setOverpayment(?Overpayment overpayment): void |
| `particulars` | `?string` | Optional | The suppliers bank account number the payment is being made to | getParticulars(): ?string | setParticulars(?string particulars): void |
| `paymentID` | `?string` | Optional | The Xero identifier for an Payment e.g. 297c2dc5-cc47-4afd-8ec8-74990b8761e9 | getPaymentID(): ?string | setPaymentID(?string paymentID): void |
| `paymentType` | [`?string(PaymentTypeEnum)`](../../doc/models/payment-type-enum.md) | Optional, Read-only | See Payment Types. | getPaymentType(): ?string | setPaymentType(?string paymentType): void |
| `prepayment` | [`?Prepayment`](../../doc/models/prepayment.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/prepayments/](http://developer.xero.com/documentation/api/prepayments/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/prepayments/](http://developer.xero.com/documentation/api/prepayments/) | getPrepayment(): ?Prepayment | setPrepayment(?Prepayment prepayment): void |
| `reference` | `?string` | Optional | An optional description for the payment e.g. Direct Debit | getReference(): ?string | setReference(?string reference): void |
| `status` | [`?string(Status6Enum)`](../../doc/models/status-6-enum.md) | Optional | The status of the payment. | getStatus(): ?string | setStatus(?string status): void |
| `statusAttributeString` | `?string` | Optional | A string to indicate if a invoice status | getStatusAttributeString(): ?string | setStatusAttributeString(?string statusAttributeString): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | UTC timestamp of last update to the payment | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\PaymentBuilder;
use XeroAccountingAPILib\Models\Builders\AccountBuilder;
use XeroAccountingAPILib\Models\BankAccountTypeEnum;
use XeroAccountingAPILib\Models\ClassEnum;

$payment = PaymentBuilder::init()
    ->account(
        AccountBuilder::init()
            ->accountID('00002304-0000-0000-0000-000000000000')
            ->addToWatchlist(false)
            ->bankAccountNumber('BankAccountNumber8')
            ->bankAccountType(BankAccountTypeEnum::PAYPAL)
            ->class(ClassEnum::LIABILITY)
            ->build()
    )
    ->amount(254.28)
    ->bankAccountNumber('BankAccountNumber6')
    ->batchPaymentID('00000000-0000-0000-0000-000000000000')
    ->code('Code6')
    ->hasAccount(false)
    ->hasValidationErrors(false)
    ->paymentID('00000000-0000-0000-0000-000000000000')
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

