
# Expense Claims

## Structure

`ExpenseClaims`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `expenseClaims` | [`?(ExpenseClaim[])`](../../doc/models/expense-claim.md) | Optional | - | getExpenseClaims(): ?array | setExpenseClaims(?array expenseClaims): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ExpenseClaimsBuilder;
use XeroAccountingAPILib\Models\Builders\ExpenseClaimBuilder;
use XeroAccountingAPILib\Models\Builders\PaymentBuilder;
use XeroAccountingAPILib\Models\Builders\AccountBuilder;
use XeroAccountingAPILib\Models\BankAccountTypeEnum;
use XeroAccountingAPILib\Models\ClassEnum;

$expenseClaims = ExpenseClaimsBuilder::init()
    ->expenseClaims(
        [
            ExpenseClaimBuilder::init()
                ->amountDue(107.24)
                ->amountPaid(37.08)
                ->expenseClaimID('00000200-0000-0000-0000-000000000000')
                ->paymentDueDate('PaymentDueDate6')
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
                ->build(),
            ExpenseClaimBuilder::init()
                ->amountDue(107.24)
                ->amountPaid(37.08)
                ->expenseClaimID('00000200-0000-0000-0000-000000000000')
                ->paymentDueDate('PaymentDueDate6')
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
                ->build(),
            ExpenseClaimBuilder::init()
                ->amountDue(107.24)
                ->amountPaid(37.08)
                ->expenseClaimID('00000200-0000-0000-0000-000000000000')
                ->paymentDueDate('PaymentDueDate6')
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
                ->build()
        ]
    )
    ->build();
```

