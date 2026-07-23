
# Quote

Find out more here: [http://developer.xero.com/documentation/api/Quotes/](http://developer.xero.com/documentation/api/Quotes/)

## Structure

`Quote`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `brandingThemeID` | `?string` | Optional | See BrandingThemes | getBrandingThemeID(): ?string | setBrandingThemeID(?string brandingThemeID): void |
| `contact` | [`?Contact`](../../doc/models/contact.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/) | getContact(): ?Contact | setContact(?Contact contact): void |
| `currencyCode` | [`?string(CurrencyCodeEnum)`](../../doc/models/currency-code-enum.md) | Optional | 3 letter alpha code for the currency – see list of currency codes | getCurrencyCode(): ?string | setCurrencyCode(?string currencyCode): void |
| `currencyRate` | `?float` | Optional | The currency rate for a multicurrency quote | getCurrencyRate(): ?float | setCurrencyRate(?float currencyRate): void |
| `date` | `?string` | Optional | Date quote was issued – YYYY-MM-DD. If the Date element is not specified it will default to the current date based on the timezone setting of the organisation | getDate(): ?string | setDate(?string date): void |
| `dateString` | `?string` | Optional | Date the quote was issued (YYYY-MM-DD) | getDateString(): ?string | setDateString(?string dateString): void |
| `expiryDate` | `?string` | Optional | Date the quote expires – YYYY-MM-DD. | getExpiryDate(): ?string | setExpiryDate(?string expiryDate): void |
| `expiryDateString` | `?string` | Optional | Date the quote expires – YYYY-MM-DD. | getExpiryDateString(): ?string | setExpiryDateString(?string expiryDateString): void |
| `lineAmountTypes` | [`?string(QuoteLineAmountTypesEnum)`](../../doc/models/quote-line-amount-types-enum.md) | Optional | Line amounts are exclusive of tax by default if you don’t specify this element. See Line Amount Types | getLineAmountTypes(): ?string | setLineAmountTypes(?string lineAmountTypes): void |
| `lineItems` | [`?(LineItem[])`](../../doc/models/line-item.md) | Optional | See LineItems | getLineItems(): ?array | setLineItems(?array lineItems): void |
| `quoteID` | `?string` | Optional | QuoteID GUID is automatically generated and is returned after create or GET. | getQuoteID(): ?string | setQuoteID(?string quoteID): void |
| `quoteNumber` | `?string` | Optional | Unique alpha numeric code identifying a quote (Max Length = 255)<br><br>**Constraints**: *Maximum Length*: `255` | getQuoteNumber(): ?string | setQuoteNumber(?string quoteNumber): void |
| `reference` | `?string` | Optional | Additional reference number<br><br>**Constraints**: *Maximum Length*: `4000` | getReference(): ?string | setReference(?string reference): void |
| `status` | [`?string(QuoteStatusCodesEnum)`](../../doc/models/quote-status-codes-enum.md) | Optional | The status of the quote. | getStatus(): ?string | setStatus(?string status): void |
| `statusAttributeString` | `?string` | Optional | A string to indicate if a invoice status | getStatusAttributeString(): ?string | setStatusAttributeString(?string statusAttributeString): void |
| `subTotal` | `?float` | Optional, Read-only | Total of quote excluding taxes. | getSubTotal(): ?float | setSubTotal(?float subTotal): void |
| `summary` | `?string` | Optional | Summary text for the quote<br><br>**Constraints**: *Maximum Length*: `3000` | getSummary(): ?string | setSummary(?string summary): void |
| `terms` | `?string` | Optional | Terms of the quote<br><br>**Constraints**: *Maximum Length*: `4000` | getTerms(): ?string | setTerms(?string terms): void |
| `title` | `?string` | Optional | Title text for the quote<br><br>**Constraints**: *Maximum Length*: `100` | getTitle(): ?string | setTitle(?string title): void |
| `total` | `?float` | Optional, Read-only | Total of Quote tax inclusive (i.e. SubTotal + TotalTax). This will be ignored if it doesn’t equal the sum of the LineAmounts | getTotal(): ?float | setTotal(?float total): void |
| `totalDiscount` | `?float` | Optional, Read-only | Total of discounts applied on the quote line items | getTotalDiscount(): ?float | setTotalDiscount(?float totalDiscount): void |
| `totalTax` | `?float` | Optional, Read-only | Total tax on quote | getTotalTax(): ?float | setTotalTax(?float totalTax): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | Last modified date UTC format | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\QuoteBuilder;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;

$quote = QuoteBuilder::init()
    ->brandingThemeID('00002508-0000-0000-0000-000000000000')
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
    ->currencyCode(CurrencyCodeEnum::SBD)
    ->currencyRate(127.62)
    ->date('Date8')
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

