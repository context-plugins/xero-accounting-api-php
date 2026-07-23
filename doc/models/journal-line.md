
# Journal Line

Find out more here: [https://developer.xero.com/documentation/api/journals#JournalLines](https://developer.xero.com/documentation/api/journals#JournalLines)

## Structure

`JournalLine`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountCode` | `?string` | Optional | See Accounts | getAccountCode(): ?string | setAccountCode(?string accountCode): void |
| `accountID` | `?string` | Optional | See Accounts | getAccountID(): ?string | setAccountID(?string accountID): void |
| `accountName` | `?string` | Optional | See AccountCodes | getAccountName(): ?string | setAccountName(?string accountName): void |
| `accountType` | [`?string(AccountTypeEnum)`](../../doc/models/account-type-enum.md) | Optional | See Account Types | getAccountType(): ?string | setAccountType(?string accountType): void |
| `description` | `?string` | Optional | The description from the source transaction line item. Only returned if populated. | getDescription(): ?string | setDescription(?string description): void |
| `grossAmount` | `?float` | Optional | Gross amount of journal line (NetAmount + TaxAmount). | getGrossAmount(): ?float | setGrossAmount(?float grossAmount): void |
| `journalLineID` | `?string` | Optional | Xero identifier for Journal | getJournalLineID(): ?string | setJournalLineID(?string journalLineID): void |
| `netAmount` | `?float` | Optional | Net amount of journal line. This will be a positive value for a debit and negative for a credit | getNetAmount(): ?float | setNetAmount(?float netAmount): void |
| `taxAmount` | `?float` | Optional, Read-only | Total tax on a journal line | getTaxAmount(): ?float | setTaxAmount(?float taxAmount): void |
| `taxName` | `?string` | Optional | see TaxRates | getTaxName(): ?string | setTaxName(?string taxName): void |
| `taxType` | `?string` | Optional | The tax type from TaxRates | getTaxType(): ?string | setTaxType(?string taxType): void |
| `trackingCategories` | [`?(TrackingCategory[])`](../../doc/models/tracking-category.md) | Optional | Optional Tracking Category – see Tracking. Any JournalLine can have a maximum of 2 <TrackingCategory> elements. | getTrackingCategories(): ?array | setTrackingCategories(?array trackingCategories): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\JournalLineBuilder;
use XeroAccountingAPILib\Models\AccountTypeEnum;

$journalLine = JournalLineBuilder::init()
    ->accountCode('90')
    ->accountID('ceef66a5-a545-413b-9312-78a53caadbc4')
    ->accountName('Checking Account')
    ->accountType(AccountTypeEnum::DIRECTCOSTS)
    ->description('My business checking account')
    ->grossAmount(4130.98)
    ->journalLineID('7be9db36-3598-4755-ba5c-c2dbc8c4a7a2')
    ->netAmount(4130.98)
    ->taxAmount(0)
    ->taxName('Tax Exempt')
    ->build();
```

