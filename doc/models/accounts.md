
# Accounts

## Structure

`Accounts`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accounts` | [`?(Account[])`](../../doc/models/account.md) | Optional | - | getAccounts(): ?array | setAccounts(?array accounts): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\AccountsBuilder;
use XeroAccountingAPILib\Models\Builders\AccountBuilder;
use XeroAccountingAPILib\Models\BankAccountTypeEnum;
use XeroAccountingAPILib\Models\ClassEnum;

$accounts = AccountsBuilder::init()
    ->accounts(
        [
            AccountBuilder::init()
                ->accountID('000025be-0000-0000-0000-000000000000')
                ->addToWatchlist(false)
                ->bankAccountNumber('BankAccountNumber6')
                ->bankAccountType(BankAccountTypeEnum::BANK)
                ->class(ClassEnum::EQUITY)
                ->build(),
            AccountBuilder::init()
                ->accountID('000025be-0000-0000-0000-000000000000')
                ->addToWatchlist(false)
                ->bankAccountNumber('BankAccountNumber6')
                ->bankAccountType(BankAccountTypeEnum::BANK)
                ->class(ClassEnum::EQUITY)
                ->build(),
            AccountBuilder::init()
                ->accountID('000025be-0000-0000-0000-000000000000')
                ->addToWatchlist(false)
                ->bankAccountNumber('BankAccountNumber6')
                ->bankAccountType(BankAccountTypeEnum::BANK)
                ->class(ClassEnum::EQUITY)
                ->build()
        ]
    )
    ->build();
```

