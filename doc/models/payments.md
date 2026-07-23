
# Payments

## Structure

`Payments`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `payments` | [`?(Payment[])`](../../doc/models/payment.md) | Optional | - | getPayments(): ?array | setPayments(?array payments): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\PaymentsBuilder;
use XeroAccountingAPILib\Models\Builders\PaymentBuilder;
use XeroAccountingAPILib\Models\Builders\AccountBuilder;
use XeroAccountingAPILib\Models\BankAccountTypeEnum;
use XeroAccountingAPILib\Models\ClassEnum;

$payments = PaymentsBuilder::init()
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
    ->build();
```

