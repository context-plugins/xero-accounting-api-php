
# Batch Payment

Find out more here: [http://developer.xero.com/documentation/api/BatchPayments/](http://developer.xero.com/documentation/api/BatchPayments/)

## Structure

`BatchPayment`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `account` | [`?Account`](../../doc/models/account.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/accounts/](http://developer.xero.com/documentation/api/accounts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/accounts/](http://developer.xero.com/documentation/api/accounts/) | getAccount(): ?Account | setAccount(?Account account): void |
| `amount` | `?float` | Optional | The amount of the payment. Must be less than or equal to the outstanding amount owing on the invoice e.g. 200.00 | getAmount(): ?float | setAmount(?float amount): void |
| `batchPaymentID` | `?string` | Optional, Read-only | The Xero generated unique identifier for the bank transaction (read-only) | getBatchPaymentID(): ?string | setBatchPaymentID(?string batchPaymentID): void |
| `code` | `?string` | Optional | (NZ Only) Optional references for the batch payment transaction. It will also show with the batch payment transaction in the bank reconciliation Find & Match screen. Depending on your individual bank, the detail may also show on the bank statement you import into Xero.<br><br>**Constraints**: *Maximum Length*: `12` | getCode(): ?string | setCode(?string code): void |
| `date` | `?string` | Optional | Date the payment is being made (YYYY-MM-DD) e.g. 2009-09-06 | getDate(): ?string | setDate(?string date): void |
| `dateString` | `?string` | Optional | Date the payment is being made (YYYY-MM-DD) e.g. 2009-09-06 | getDateString(): ?string | setDateString(?string dateString): void |
| `details` | `?string` | Optional | (Non-NZ Only) These details are sent to the org’s bank as a reference for the batch payment transaction. They will also show with the batch payment transaction in the bank reconciliation Find & Match screen. Depending on your individual bank, the detail may also show on the bank statement imported into Xero. Maximum field length = 18 | getDetails(): ?string | setDetails(?string details): void |
| `isReconciled` | `?string` | Optional, Read-only | Booelan that tells you if the batch payment has been reconciled (read-only) | getIsReconciled(): ?string | setIsReconciled(?string isReconciled): void |
| `narrative` | `?string` | Optional | (UK Only) Only shows on the statement line in Xero. Max length =18<br><br>**Constraints**: *Maximum Length*: `18` | getNarrative(): ?string | setNarrative(?string narrative): void |
| `particulars` | `?string` | Optional | (NZ Only) Optional references for the batch payment transaction. It will also show with the batch payment transaction in the bank reconciliation Find & Match screen. Depending on your individual bank, the detail may also show on the bank statement you import into Xero.<br><br>**Constraints**: *Maximum Length*: `12` | getParticulars(): ?string | setParticulars(?string particulars): void |
| `payments` | [`?(Payment[])`](../../doc/models/payment.md) | Optional | An array of payments | getPayments(): ?array | setPayments(?array payments): void |
| `reference` | `?string` | Optional | (NZ Only) Optional references for the batch payment transaction. It will also show with the batch payment transaction in the bank reconciliation Find & Match screen. Depending on your individual bank, the detail may also show on the bank statement you import into Xero.<br><br>**Constraints**: *Maximum Length*: `255` | getReference(): ?string | setReference(?string reference): void |
| `status` | [`?string(Status9Enum)`](../../doc/models/status-9-enum.md) | Optional, Read-only | AUTHORISED or DELETED (read-only). New batch payments will have a status of AUTHORISED. It is not possible to delete batch payments via the API. | getStatus(): ?string | setStatus(?string status): void |
| `totalAmount` | `?string` | Optional, Read-only | The total of the payments that make up the batch (read-only) | getTotalAmount(): ?string | setTotalAmount(?string totalAmount): void |
| `type` | [`?string(Type6Enum)`](../../doc/models/type-6-enum.md) | Optional, Read-only | PAYBATCH for bill payments or RECBATCH for sales invoice payments (read-only) | getType(): ?string | setType(?string type): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | UTC timestamp of last update to the payment | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\BatchPaymentBuilder;
use XeroAccountingAPILib\Models\Builders\AccountBuilder;
use XeroAccountingAPILib\Models\BankAccountTypeEnum;
use XeroAccountingAPILib\Models\ClassEnum;

$batchPayment = BatchPaymentBuilder::init()
    ->account(
        AccountBuilder::init()
            ->accountID('00002304-0000-0000-0000-000000000000')
            ->addToWatchlist(false)
            ->bankAccountNumber('BankAccountNumber8')
            ->bankAccountType(BankAccountTypeEnum::PAYPAL)
            ->class(ClassEnum::LIABILITY)
            ->build()
    )
    ->amount(174.5)
    ->batchPaymentID('000019f4-0000-0000-0000-000000000000')
    ->code('Code8')
    ->date('Date6')
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

