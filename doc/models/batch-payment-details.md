
# Batch Payment Details

Bank details for use on a batch payment stored with each contact

Find out more here: [http://developer.xero.com/documentation/api/Contact/](http://developer.xero.com/documentation/api/Contact/)

## Structure

`BatchPaymentDetails`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `bankAccountName` | `?string` | Optional | Name of bank for use with Batch Payments | getBankAccountName(): ?string | setBankAccountName(?string bankAccountName): void |
| `bankAccountNumber` | `?string` | Optional | Bank account number for use with Batch Payments | getBankAccountNumber(): ?string | setBankAccountNumber(?string bankAccountNumber): void |
| `code` | `?string` | Optional | (NZ Only) Optional references for the batch payment transaction. It will also show with the batch payment transaction in the bank reconciliation Find & Match screen. Depending on your individual bank, the detail may also show on the bank statement you import into Xero.<br><br>**Constraints**: *Maximum Length*: `12` | getCode(): ?string | setCode(?string code): void |
| `details` | `?string` | Optional | (Non-NZ Only) These details are sent to the org’s bank as a reference for the batch payment transaction. They will also show with the batch payment transaction in the bank reconciliation Find & Match screen. Depending on your individual bank, the detail may also show on the bank statement imported into Xero. Maximum field length = 18 | getDetails(): ?string | setDetails(?string details): void |
| `reference` | `?string` | Optional | (NZ Only) Optional references for the batch payment transaction. It will also show with the batch payment transaction in the bank reconciliation Find & Match screen. Depending on your individual bank, the detail may also show on the bank statement you import into Xero.<br><br>**Constraints**: *Maximum Length*: `12` | getReference(): ?string | setReference(?string reference): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\BatchPaymentDetailsBuilder;

$batchPaymentDetails = BatchPaymentDetailsBuilder::init()
    ->bankAccountName('ACME Bank')
    ->bankAccountNumber('123-456-1111111')
    ->code('ABC')
    ->details('Hello World')
    ->reference('Foobar')
    ->build();
```

