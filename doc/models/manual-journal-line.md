
# Manual Journal Line

Find out more here: [http://developer.xero.com/documentation/api/manual-journals/](http://developer.xero.com/documentation/api/manual-journals/)

## Structure

`ManualJournalLine`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountCode` | `?string` | Optional | See Accounts | getAccountCode(): ?string | setAccountCode(?string accountCode): void |
| `accountID` | `?string` | Optional | See Accounts | getAccountID(): ?string | setAccountID(?string accountID): void |
| `description` | `?string` | Optional | Description for journal line | getDescription(): ?string | setDescription(?string description): void |
| `isBlank` | `?bool` | Optional | is the line blank | getIsBlank(): ?bool | setIsBlank(?bool isBlank): void |
| `lineAmount` | `?float` | Optional | total for line. Debits are positive, credits are negative value | getLineAmount(): ?float | setLineAmount(?float lineAmount): void |
| `taxAmount` | `?float` | Optional, Read-only | The calculated tax amount based on the TaxType and LineAmount | getTaxAmount(): ?float | setTaxAmount(?float taxAmount): void |
| `taxType` | `?string` | Optional | The tax type from TaxRates | getTaxType(): ?string | setTaxType(?string taxType): void |
| `tracking` | [`?(TrackingCategory[])`](../../doc/models/tracking-category.md) | Optional | Optional Tracking Category – see Tracking. Any JournalLine can have a maximum of 2 <TrackingCategory> elements. | getTracking(): ?array | setTracking(?array tracking): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ManualJournalLineBuilder;

$manualJournalLine = ManualJournalLineBuilder::init()
    ->accountCode('720')
    ->accountID('000019e2-0000-0000-0000-000000000000')
    ->description('Coded incorrectly Office Equipment should be Computer Equipment')
    ->isBlank(false)
    ->lineAmount(-2569)
    ->taxAmount(0)
    ->build();
```

