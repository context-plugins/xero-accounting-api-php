
# Bank Transactions

## Structure

`BankTransactions`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `bankTransactions` | [`?(BankTransaction[])`](../../doc/models/bank-transaction.md) | Optional | - | getBankTransactions(): ?array | setBankTransactions(?array bankTransactions): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\BankTransactionsBuilder;
use XeroAccountingAPILib\Models\Builders\BankTransactionBuilder;
use XeroAccountingAPILib\Models\Builders\AccountBuilder;
use XeroAccountingAPILib\Models\BankAccountTypeEnum;
use XeroAccountingAPILib\Models\ClassEnum;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;
use XeroAccountingAPILib\Models\Builders\LineItemBuilder;
use XeroAccountingAPILib\Models\Type5Enum;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;

$bankTransactions = BankTransactionsBuilder::init()
    ->bankTransactions(
        [
            BankTransactionBuilder::init(
                AccountBuilder::init()
                    ->accountID('0000081e-0000-0000-0000-000000000000')
                    ->addToWatchlist(false)
                    ->bankAccountNumber('BankAccountNumber2')
                    ->bankAccountType(BankAccountTypeEnum::BANK)
                    ->class(ClassEnum::EXPENSE)
                    ->build(),
                [
                    LineItemBuilder::init()
                        ->accountCode('AccountCode0')
                        ->description('Description0')
                        ->discountAmount(58.88)
                        ->discountRate(40.9)
                        ->itemCode('ItemCode6')
                        ->build()
                ],
                Type5Enum::RECEIVE
            )
                ->bankTransactionID('00001c9c-0000-0000-0000-000000000000')
                ->contact(
                    ContactBuilder::init()
                        ->accountNumber('AccountNumber2')
                        ->accountsPayableTaxType('AccountsPayableTaxType2')
                        ->accountsReceivableTaxType('AccountsReceivableTaxType6')
                        ->addresses(
                            [
                                AddressBuilder::init()
                                    ->addressLine1('AddressLine14')
                                    ->addressLine2('AddressLine20')
                                    ->addressLine3('AddressLine38')
                                    ->addressLine4('AddressLine46')
                                    ->addressType(AddressTypeEnum::POBOX)
                                    ->build()
                            ]
                        )
                        ->attachments(
                            [
                                AttachmentBuilder::init()
                                    ->attachmentID('00000714-0000-0000-0000-000000000000')
                                    ->contentLength(34)
                                    ->fileName('FileName6')
                                    ->includeOnline(false)
                                    ->mimeType('MimeType6')
                                    ->build(),
                                AttachmentBuilder::init()
                                    ->attachmentID('00000714-0000-0000-0000-000000000000')
                                    ->contentLength(34)
                                    ->fileName('FileName6')
                                    ->includeOnline(false)
                                    ->mimeType('MimeType6')
                                    ->build()
                            ]
                        )
                        ->build()
                )
                ->currencyCode(CurrencyCodeEnum::LBP)
                ->currencyRate(143.72)
                ->date('Date8')
                ->build(),
            BankTransactionBuilder::init(
                AccountBuilder::init()
                    ->accountID('0000081e-0000-0000-0000-000000000000')
                    ->addToWatchlist(false)
                    ->bankAccountNumber('BankAccountNumber2')
                    ->bankAccountType(BankAccountTypeEnum::BANK)
                    ->class(ClassEnum::EXPENSE)
                    ->build(),
                [
                    LineItemBuilder::init()
                        ->accountCode('AccountCode0')
                        ->description('Description0')
                        ->discountAmount(58.88)
                        ->discountRate(40.9)
                        ->itemCode('ItemCode6')
                        ->build()
                ],
                Type5Enum::RECEIVE
            )
                ->bankTransactionID('00001c9c-0000-0000-0000-000000000000')
                ->contact(
                    ContactBuilder::init()
                        ->accountNumber('AccountNumber2')
                        ->accountsPayableTaxType('AccountsPayableTaxType2')
                        ->accountsReceivableTaxType('AccountsReceivableTaxType6')
                        ->addresses(
                            [
                                AddressBuilder::init()
                                    ->addressLine1('AddressLine14')
                                    ->addressLine2('AddressLine20')
                                    ->addressLine3('AddressLine38')
                                    ->addressLine4('AddressLine46')
                                    ->addressType(AddressTypeEnum::POBOX)
                                    ->build()
                            ]
                        )
                        ->attachments(
                            [
                                AttachmentBuilder::init()
                                    ->attachmentID('00000714-0000-0000-0000-000000000000')
                                    ->contentLength(34)
                                    ->fileName('FileName6')
                                    ->includeOnline(false)
                                    ->mimeType('MimeType6')
                                    ->build(),
                                AttachmentBuilder::init()
                                    ->attachmentID('00000714-0000-0000-0000-000000000000')
                                    ->contentLength(34)
                                    ->fileName('FileName6')
                                    ->includeOnline(false)
                                    ->mimeType('MimeType6')
                                    ->build()
                            ]
                        )
                        ->build()
                )
                ->currencyCode(CurrencyCodeEnum::LBP)
                ->currencyRate(143.72)
                ->date('Date8')
                ->build(),
            BankTransactionBuilder::init(
                AccountBuilder::init()
                    ->accountID('0000081e-0000-0000-0000-000000000000')
                    ->addToWatchlist(false)
                    ->bankAccountNumber('BankAccountNumber2')
                    ->bankAccountType(BankAccountTypeEnum::BANK)
                    ->class(ClassEnum::EXPENSE)
                    ->build(),
                [
                    LineItemBuilder::init()
                        ->accountCode('AccountCode0')
                        ->description('Description0')
                        ->discountAmount(58.88)
                        ->discountRate(40.9)
                        ->itemCode('ItemCode6')
                        ->build()
                ],
                Type5Enum::RECEIVE
            )
                ->bankTransactionID('00001c9c-0000-0000-0000-000000000000')
                ->contact(
                    ContactBuilder::init()
                        ->accountNumber('AccountNumber2')
                        ->accountsPayableTaxType('AccountsPayableTaxType2')
                        ->accountsReceivableTaxType('AccountsReceivableTaxType6')
                        ->addresses(
                            [
                                AddressBuilder::init()
                                    ->addressLine1('AddressLine14')
                                    ->addressLine2('AddressLine20')
                                    ->addressLine3('AddressLine38')
                                    ->addressLine4('AddressLine46')
                                    ->addressType(AddressTypeEnum::POBOX)
                                    ->build()
                            ]
                        )
                        ->attachments(
                            [
                                AttachmentBuilder::init()
                                    ->attachmentID('00000714-0000-0000-0000-000000000000')
                                    ->contentLength(34)
                                    ->fileName('FileName6')
                                    ->includeOnline(false)
                                    ->mimeType('MimeType6')
                                    ->build(),
                                AttachmentBuilder::init()
                                    ->attachmentID('00000714-0000-0000-0000-000000000000')
                                    ->contentLength(34)
                                    ->fileName('FileName6')
                                    ->includeOnline(false)
                                    ->mimeType('MimeType6')
                                    ->build()
                            ]
                        )
                        ->build()
                )
                ->currencyCode(CurrencyCodeEnum::LBP)
                ->currencyRate(143.72)
                ->date('Date8')
                ->build()
        ]
    )
    ->build();
```

