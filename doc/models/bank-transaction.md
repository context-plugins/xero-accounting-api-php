
# Bank Transaction

Find out more here: [http://developer.xero.com/documentation/api/banktransactions/](http://developer.xero.com/documentation/api/banktransactions/)

## Structure

`BankTransaction`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `bankAccount` | [`Account`](../../doc/models/account.md) | Required | Find out more here: [http://developer.xero.com/documentation/api/accounts/](http://developer.xero.com/documentation/api/accounts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/accounts/](http://developer.xero.com/documentation/api/accounts/) | getBankAccount(): Account | setBankAccount(Account bankAccount): void |
| `bankTransactionID` | `?string` | Optional | Xero generated unique identifier for bank transaction | getBankTransactionID(): ?string | setBankTransactionID(?string bankTransactionID): void |
| `contact` | [`?Contact`](../../doc/models/contact.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/) | getContact(): ?Contact | setContact(?Contact contact): void |
| `currencyCode` | [`?string(CurrencyCodeEnum)`](../../doc/models/currency-code-enum.md) | Optional | 3 letter alpha code for the currency – see list of currency codes | getCurrencyCode(): ?string | setCurrencyCode(?string currencyCode): void |
| `currencyRate` | `?float` | Optional | Exchange rate to base currency when money is spent or received. e.g.0.7500 Only used for bank transactions in non base currency. If this isn’t specified for non base currency accounts then either the user-defined rate (preference) or the XE.com day rate will be used. Setting currency is only supported on overpayments. | getCurrencyRate(): ?float | setCurrencyRate(?float currencyRate): void |
| `date` | `?string` | Optional | Date of transaction – YYYY-MM-DD | getDate(): ?string | setDate(?string date): void |
| `hasAttachments` | `?bool` | Optional, Read-only | Boolean to indicate if a bank transaction has an attachment<br><br>**Default**: `false` | getHasAttachments(): ?bool | setHasAttachments(?bool hasAttachments): void |
| `isReconciled` | `?bool` | Optional | Boolean to show if transaction is reconciled | getIsReconciled(): ?bool | setIsReconciled(?bool isReconciled): void |
| `lineAmountTypes` | [`?string(LineAmountTypesEnum)`](../../doc/models/line-amount-types-enum.md) | Optional | Line amounts are exclusive of tax by default if you don’t specify this element. See Line Amount Types | getLineAmountTypes(): ?string | setLineAmountTypes(?string lineAmountTypes): void |
| `lineItems` | [`LineItem[]`](../../doc/models/line-item.md) | Required | See LineItems | getLineItems(): array | setLineItems(array lineItems): void |
| `overpaymentID` | `?string` | Optional, Read-only | Xero generated unique identifier for an Overpayment. This will be returned on BankTransactions with a Type of SPEND-OVERPAYMENT or RECEIVE-OVERPAYMENT | getOverpaymentID(): ?string | setOverpaymentID(?string overpaymentID): void |
| `prepaymentID` | `?string` | Optional, Read-only | Xero generated unique identifier for a Prepayment. This will be returned on BankTransactions with a Type of SPEND-PREPAYMENT or RECEIVE-PREPAYMENT | getPrepaymentID(): ?string | setPrepaymentID(?string prepaymentID): void |
| `reference` | `?string` | Optional | Reference for the transaction. Only supported for SPEND and RECEIVE transactions. | getReference(): ?string | setReference(?string reference): void |
| `status` | [`?string(Status8Enum)`](../../doc/models/status-8-enum.md) | Optional | See Bank Transaction Status Codes | getStatus(): ?string | setStatus(?string status): void |
| `statusAttributeString` | `?string` | Optional | A string to indicate if a invoice status | getStatusAttributeString(): ?string | setStatusAttributeString(?string statusAttributeString): void |
| `subTotal` | `?float` | Optional | Total of bank transaction excluding taxes | getSubTotal(): ?float | setSubTotal(?float subTotal): void |
| `total` | `?float` | Optional | Total of bank transaction tax inclusive | getTotal(): ?float | setTotal(?float total): void |
| `totalTax` | `?float` | Optional | Total tax on bank transaction | getTotalTax(): ?float | setTotalTax(?float totalTax): void |
| `type` | [`string(Type5Enum)`](../../doc/models/type-5-enum.md) | Required | See Bank Transaction Types | getType(): string | setType(string type): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | Last modified date UTC format | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `url` | `?string` | Optional | URL link to a source document – shown as “Go to App Name” | getUrl(): ?string | setUrl(?string url): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |

## Example

```php
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

$bankTransaction = BankTransactionBuilder::init(
    AccountBuilder::init()
        ->accountID('00000000-0000-0000-0000-000000000000')
        ->addToWatchlist(false)
        ->bankAccountNumber('BankAccountNumber2')
        ->bankAccountType(BankAccountTypeEnum::BANK)
        ->class(ClassEnum::EXPENSE)
        ->code('4400')
        ->hasAttachments(false)
        ->name('Food Sales')
        ->updatedDateUTC('/Date(1573755038314)/')
        ->build(),
    [
        LineItemBuilder::init()
            ->accountCode('AccountCode0')
            ->description('Description0')
            ->discountAmount(58.88)
            ->discountRate(40.9)
            ->itemCode('ItemCode6')
            ->lineItemID('00000000-0000-0000-0000-000000000000')
            ->repeatingInvoiceID('00000000-0000-0000-0000-000000000000')
            ->build()
    ],
    Type5Enum::RECEIVETRANSFER
)
    ->bankTransactionID('00000000-0000-0000-0000-000000000000')
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
    ->currencyCode(CurrencyCodeEnum::COP)
    ->currencyRate(58.46)
    ->date('Date0')
    ->hasAttachments(false)
    ->overpaymentID('00000000-0000-0000-0000-000000000000')
    ->prepaymentID('00000000-0000-0000-0000-000000000000')
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

