
# Bank Transfers

## Structure

`BankTransfers`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `bankTransfers` | [`?(BankTransfer[])`](../../doc/models/bank-transfer.md) | Optional | - | getBankTransfers(): ?array | setBankTransfers(?array bankTransfers): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\BankTransfersBuilder;
use XeroAccountingAPILib\Models\Builders\BankTransferBuilder;
use XeroAccountingAPILib\Models\Builders\AccountBuilder;
use XeroAccountingAPILib\Models\BankAccountTypeEnum;
use XeroAccountingAPILib\Models\ClassEnum;

$bankTransfers = BankTransfersBuilder::init()
    ->bankTransfers(
        [
            BankTransferBuilder::init(
                103.7,
                AccountBuilder::init()
                    ->accountID('00001364-0000-0000-0000-000000000000')
                    ->addToWatchlist(false)
                    ->bankAccountNumber('BankAccountNumber8')
                    ->bankAccountType(BankAccountTypeEnum::PAYPAL)
                    ->class(ClassEnum::LIABILITY)
                    ->build(),
                AccountBuilder::init()
                    ->accountID('000014a2-0000-0000-0000-000000000000')
                    ->addToWatchlist(false)
                    ->bankAccountNumber('BankAccountNumber6')
                    ->bankAccountType(BankAccountTypeEnum::BANK)
                    ->class(ClassEnum::REVENUE)
                    ->build()
            )
                ->bankTransferID('00001594-0000-0000-0000-000000000000')
                ->createdDateUTC('CreatedDateUTC6')
                ->currencyRate(15.4)
                ->date('Date6')
                ->fromBankTransactionID('00001682-0000-0000-0000-000000000000')
                ->build(),
            BankTransferBuilder::init(
                103.7,
                AccountBuilder::init()
                    ->accountID('00001364-0000-0000-0000-000000000000')
                    ->addToWatchlist(false)
                    ->bankAccountNumber('BankAccountNumber8')
                    ->bankAccountType(BankAccountTypeEnum::PAYPAL)
                    ->class(ClassEnum::LIABILITY)
                    ->build(),
                AccountBuilder::init()
                    ->accountID('000014a2-0000-0000-0000-000000000000')
                    ->addToWatchlist(false)
                    ->bankAccountNumber('BankAccountNumber6')
                    ->bankAccountType(BankAccountTypeEnum::BANK)
                    ->class(ClassEnum::REVENUE)
                    ->build()
            )
                ->bankTransferID('00001594-0000-0000-0000-000000000000')
                ->createdDateUTC('CreatedDateUTC6')
                ->currencyRate(15.4)
                ->date('Date6')
                ->fromBankTransactionID('00001682-0000-0000-0000-000000000000')
                ->build()
        ]
    )
    ->build();
```

