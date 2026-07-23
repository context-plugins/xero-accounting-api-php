
# Expense Claim

Find out more here: [http://developer.xero.com/documentation/api/expense-claims/](http://developer.xero.com/documentation/api/expense-claims/)

## Structure

`ExpenseClaim`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amountDue` | `?float` | Optional, Read-only | The amount due to be paid for an expense claim | getAmountDue(): ?float | setAmountDue(?float amountDue): void |
| `amountPaid` | `?float` | Optional, Read-only | The amount still to pay for an expense claim | getAmountPaid(): ?float | setAmountPaid(?float amountPaid): void |
| `expenseClaimID` | `?string` | Optional | Xero generated unique identifier for an expense claim | getExpenseClaimID(): ?string | setExpenseClaimID(?string expenseClaimID): void |
| `paymentDueDate` | `?string` | Optional, Read-only | The date when the expense claim is due to be paid YYYY-MM-DD | getPaymentDueDate(): ?string | setPaymentDueDate(?string paymentDueDate): void |
| `payments` | [`?(Payment[])`](../../doc/models/payment.md) | Optional | See Payments | getPayments(): ?array | setPayments(?array payments): void |
| `receiptID` | `?string` | Optional | The Xero identifier for the Receipt e.g. e59a2c7f-1306-4078-a0f3-73537afcbba9 | getReceiptID(): ?string | setReceiptID(?string receiptID): void |
| `receipts` | [`?(Receipt[])`](../../doc/models/receipt.md) | Optional | - | getReceipts(): ?array | setReceipts(?array receipts): void |
| `reportingDate` | `?string` | Optional, Read-only | The date the expense claim will be reported in Xero YYYY-MM-DD | getReportingDate(): ?string | setReportingDate(?string reportingDate): void |
| `status` | [`?string(Status12Enum)`](../../doc/models/status-12-enum.md) | Optional | Current status of an expense claim – see status types | getStatus(): ?string | setStatus(?string status): void |
| `total` | `?float` | Optional, Read-only | The total of an expense claim being paid | getTotal(): ?float | setTotal(?float total): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | Last modified date UTC format | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `user` | [`?User`](../../doc/models/user.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/users/](http://developer.xero.com/documentation/api/users/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/users/](http://developer.xero.com/documentation/api/users/) | getUser(): ?User | setUser(?User user): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ExpenseClaimBuilder;
use XeroAccountingAPILib\Models\Builders\PaymentBuilder;
use XeroAccountingAPILib\Models\Builders\AccountBuilder;
use XeroAccountingAPILib\Models\BankAccountTypeEnum;
use XeroAccountingAPILib\Models\ClassEnum;

$expenseClaim = ExpenseClaimBuilder::init()
    ->amountDue(152.9)
    ->amountPaid(82.74)
    ->expenseClaimID('000013d6-0000-0000-0000-000000000000')
    ->paymentDueDate('PaymentDueDate2')
    ->payments(
        [
            PaymentBuilder::init()
                ->account(
                    AccountBuilder::init()
                        ->accountID('00002304-0000-0000-0000-000000000000')
                        ->addToWatchlist(false)
                        ->bankAccountNumber('BankAccountNumber8')
                        ->bankAccountType(BankAccountTypeEnum::PAYPAL)
                        ->class(ClassEnum::LIABILITY)
                        ->build()
                )
                ->amount(24.8)
                ->bankAccountNumber('BankAccountNumber8')
                ->batchPaymentID('0000068a-0000-0000-0000-000000000000')
                ->code('Code8')
                ->build(),
            PaymentBuilder::init()
                ->account(
                    AccountBuilder::init()
                        ->accountID('00002304-0000-0000-0000-000000000000')
                        ->addToWatchlist(false)
                        ->bankAccountNumber('BankAccountNumber8')
                        ->bankAccountType(BankAccountTypeEnum::PAYPAL)
                        ->class(ClassEnum::LIABILITY)
                        ->build()
                )
                ->amount(24.8)
                ->bankAccountNumber('BankAccountNumber8')
                ->batchPaymentID('0000068a-0000-0000-0000-000000000000')
                ->code('Code8')
                ->build()
        ]
    )
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

