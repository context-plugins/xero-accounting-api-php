
# Account

Find out more here: [http://developer.xero.com/documentation/api/accounts/](http://developer.xero.com/documentation/api/accounts/)

## Structure

`Account`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountID` | `?string` | Optional | The Xero identifier for an account – specified as a string following  the endpoint name   e.g. /297c2dc5-cc47-4afd-8ec8-74990b8761e9 | getAccountID(): ?string | setAccountID(?string accountID): void |
| `addToWatchlist` | `?bool` | Optional | Boolean – describes whether the account is shown in the watchlist widget on the dashboard | getAddToWatchlist(): ?bool | setAddToWatchlist(?bool addToWatchlist): void |
| `bankAccountNumber` | `?string` | Optional | For bank accounts only (Account Type BANK) | getBankAccountNumber(): ?string | setBankAccountNumber(?string bankAccountNumber): void |
| `bankAccountType` | [`?string(BankAccountTypeEnum)`](../../doc/models/bank-account-type-enum.md) | Optional | For bank accounts only. See Bank Account types | getBankAccountType(): ?string | setBankAccountType(?string bankAccountType): void |
| `class` | [`?string(ClassEnum)`](../../doc/models/m-class-enum.md) | Optional, Read-only | See Account Class Types | getClass(): ?string | setClass(?string class): void |
| `code` | `?string` | Optional | Customer defined alpha numeric account code e.g 200 or SALES (max length = 10) | getCode(): ?string | setCode(?string code): void |
| `currencyCode` | [`?string(CurrencyCodeEnum)`](../../doc/models/currency-code-enum.md) | Optional | 3 letter alpha code for the currency – see list of currency codes | getCurrencyCode(): ?string | setCurrencyCode(?string currencyCode): void |
| `description` | `?string` | Optional | Description of the Account. Valid for all types of accounts except bank accounts (max length = 4000) | getDescription(): ?string | setDescription(?string description): void |
| `enablePaymentsToAccount` | `?bool` | Optional | Boolean – describes whether account can have payments applied to it | getEnablePaymentsToAccount(): ?bool | setEnablePaymentsToAccount(?bool enablePaymentsToAccount): void |
| `hasAttachments` | `?bool` | Optional, Read-only | boolean to indicate if an account has an attachment (read only)<br><br>**Default**: `false` | getHasAttachments(): ?bool | setHasAttachments(?bool hasAttachments): void |
| `name` | `?string` | Optional | Name of account (max length = 150)<br><br>**Constraints**: *Maximum Length*: `150` | getName(): ?string | setName(?string name): void |
| `reportingCode` | `?string` | Optional | Shown if set | getReportingCode(): ?string | setReportingCode(?string reportingCode): void |
| `reportingCodeName` | `?string` | Optional, Read-only | Shown if set | getReportingCodeName(): ?string | setReportingCodeName(?string reportingCodeName): void |
| `showInExpenseClaims` | `?bool` | Optional | Boolean – describes whether account code is available for use with expense claims | getShowInExpenseClaims(): ?bool | setShowInExpenseClaims(?bool showInExpenseClaims): void |
| `status` | [`?string(StatusEnum)`](../../doc/models/status-enum.md) | Optional | Accounts with a status of ACTIVE can be updated to ARCHIVED. See Account Status Codes | getStatus(): ?string | setStatus(?string status): void |
| `systemAccount` | [`?string(SystemAccountEnum)`](../../doc/models/system-account-enum.md) | Optional, Read-only | If this is a system account then this element is returned. See System Account types. Note that non-system accounts may have this element set as either “” or null. | getSystemAccount(): ?string | setSystemAccount(?string systemAccount): void |
| `taxType` | `?string` | Optional | The tax type from TaxRates | getTaxType(): ?string | setTaxType(?string taxType): void |
| `type` | [`?string(AccountTypeEnum)`](../../doc/models/account-type-enum.md) | Optional | See Account Types | getType(): ?string | setType(?string type): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | Last modified date UTC format | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\AccountBuilder;
use XeroAccountingAPILib\Models\BankAccountTypeEnum;
use XeroAccountingAPILib\Models\ClassEnum;

$account = AccountBuilder::init()
    ->accountID('00000000-0000-0000-0000-000000000000')
    ->addToWatchlist(false)
    ->bankAccountNumber('BankAccountNumber0')
    ->bankAccountType(BankAccountTypeEnum::PAYPAL)
    ->class(ClassEnum::ASSET)
    ->code('4400')
    ->hasAttachments(false)
    ->name('Food Sales')
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

