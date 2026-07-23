
# Bank Transfer

Find out more here: [http://developer.xero.com/documentation/api/bank-transfers/](http://developer.xero.com/documentation/api/bank-transfers/)

## Structure

`BankTransfer`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | `float` | Required | amount of the transaction | getAmount(): float | setAmount(float amount): void |
| `bankTransferID` | `?string` | Optional, Read-only | The identifier of the Bank Transfer | getBankTransferID(): ?string | setBankTransferID(?string bankTransferID): void |
| `createdDateUTC` | `?string` | Optional, Read-only | UTC timestamp of creation date of bank transfer | getCreatedDateUTC(): ?string | setCreatedDateUTC(?string createdDateUTC): void |
| `currencyRate` | `?float` | Optional, Read-only | The currency rate | getCurrencyRate(): ?float | setCurrencyRate(?float currencyRate): void |
| `date` | `?string` | Optional | The date of the Transfer YYYY-MM-DD | getDate(): ?string | setDate(?string date): void |
| `fromBankAccount` | [`Account`](../../doc/models/account.md) | Required | Find out more here: [http://developer.xero.com/documentation/api/accounts/](http://developer.xero.com/documentation/api/accounts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/accounts/](http://developer.xero.com/documentation/api/accounts/) | getFromBankAccount(): Account | setFromBankAccount(Account fromBankAccount): void |
| `fromBankTransactionID` | `?string` | Optional, Read-only | The Bank Transaction ID for the source account | getFromBankTransactionID(): ?string | setFromBankTransactionID(?string fromBankTransactionID): void |
| `hasAttachments` | `?bool` | Optional, Read-only | Boolean to indicate if a Bank Transfer has an attachment<br><br>**Default**: `false` | getHasAttachments(): ?bool | setHasAttachments(?bool hasAttachments): void |
| `toBankAccount` | [`Account`](../../doc/models/account.md) | Required | Find out more here: [http://developer.xero.com/documentation/api/accounts/](http://developer.xero.com/documentation/api/accounts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/accounts/](http://developer.xero.com/documentation/api/accounts/) | getToBankAccount(): Account | setToBankAccount(Account toBankAccount): void |
| `toBankTransactionID` | `?string` | Optional, Read-only | The Bank Transaction ID for the destination account | getToBankTransactionID(): ?string | setToBankTransactionID(?string toBankTransactionID): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\BankTransferBuilder;
use XeroAccountingAPILib\Models\Builders\AccountBuilder;
use XeroAccountingAPILib\Models\BankAccountTypeEnum;
use XeroAccountingAPILib\Models\ClassEnum;

$bankTransfer = BankTransferBuilder::init(
    115.42,
    AccountBuilder::init()
        ->accountID('00000000-0000-0000-0000-000000000000')
        ->addToWatchlist(false)
        ->bankAccountNumber('BankAccountNumber8')
        ->bankAccountType(BankAccountTypeEnum::PAYPAL)
        ->class(ClassEnum::LIABILITY)
        ->code('4400')
        ->hasAttachments(false)
        ->name('Food Sales')
        ->updatedDateUTC('/Date(1573755038314)/')
        ->build(),
    AccountBuilder::init()
        ->accountID('00000000-0000-0000-0000-000000000000')
        ->addToWatchlist(false)
        ->bankAccountNumber('BankAccountNumber6')
        ->bankAccountType(BankAccountTypeEnum::BANK)
        ->class(ClassEnum::REVENUE)
        ->code('4400')
        ->hasAttachments(false)
        ->name('Food Sales')
        ->updatedDateUTC('/Date(1573755038314)/')
        ->build()
)
    ->bankTransferID('000004e0-0000-0000-0000-000000000000')
    ->createdDateUTC('/Date(1573755038314)/')
    ->currencyRate(27.12)
    ->date('Date8')
    ->fromBankTransactionID('000009e6-0000-0000-0000-000000000000')
    ->hasAttachments(false)
    ->build();
```

