
# Batch Payments

## Structure

`BatchPayments`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `batchPayments` | [`?(BatchPayment[])`](../../doc/models/batch-payment.md) | Optional | - | getBatchPayments(): ?array | setBatchPayments(?array batchPayments): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\BatchPaymentsBuilder;
use XeroAccountingAPILib\Models\Builders\BatchPaymentBuilder;
use XeroAccountingAPILib\Models\Builders\AccountBuilder;
use XeroAccountingAPILib\Models\BankAccountTypeEnum;
use XeroAccountingAPILib\Models\ClassEnum;

$batchPayments = BatchPaymentsBuilder::init()
    ->batchPayments(
        [
            BatchPaymentBuilder::init()
                ->account(
                    AccountBuilder::init()
                        ->accountID('00002304-0000-0000-0000-000000000000')
                        ->addToWatchlist(false)
                        ->bankAccountNumber('BankAccountNumber8')
                        ->bankAccountType(BankAccountTypeEnum::PAYPAL)
                        ->class(ClassEnum::LIABILITY)
                        ->build()
                )
                ->amount(88.64)
                ->batchPaymentID('00001f7a-0000-0000-0000-000000000000')
                ->code('Code2')
                ->date('Date0')
                ->build(),
            BatchPaymentBuilder::init()
                ->account(
                    AccountBuilder::init()
                        ->accountID('00002304-0000-0000-0000-000000000000')
                        ->addToWatchlist(false)
                        ->bankAccountNumber('BankAccountNumber8')
                        ->bankAccountType(BankAccountTypeEnum::PAYPAL)
                        ->class(ClassEnum::LIABILITY)
                        ->build()
                )
                ->amount(88.64)
                ->batchPaymentID('00001f7a-0000-0000-0000-000000000000')
                ->code('Code2')
                ->date('Date0')
                ->build(),
            BatchPaymentBuilder::init()
                ->account(
                    AccountBuilder::init()
                        ->accountID('00002304-0000-0000-0000-000000000000')
                        ->addToWatchlist(false)
                        ->bankAccountNumber('BankAccountNumber8')
                        ->bankAccountType(BankAccountTypeEnum::PAYPAL)
                        ->class(ClassEnum::LIABILITY)
                        ->build()
                )
                ->amount(88.64)
                ->batchPaymentID('00001f7a-0000-0000-0000-000000000000')
                ->code('Code2')
                ->date('Date0')
                ->build()
        ]
    )
    ->build();
```

