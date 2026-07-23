
# Invoice

Find out more here: [http://developer.xero.com/documentation/api/invoices/](http://developer.xero.com/documentation/api/invoices/)

## Structure

`Invoice`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amountCredited` | `?float` | Optional, Read-only | Sum of all credit notes, over-payments and pre-payments applied to invoice | getAmountCredited(): ?float | setAmountCredited(?float amountCredited): void |
| `amountDue` | `?float` | Optional, Read-only | Amount remaining to be paid on invoice | getAmountDue(): ?float | setAmountDue(?float amountDue): void |
| `amountPaid` | `?float` | Optional, Read-only | Sum of payments received for invoice | getAmountPaid(): ?float | setAmountPaid(?float amountPaid): void |
| `attachments` | [`?(Attachment[])`](../../doc/models/attachment.md) | Optional | Displays array of attachments from the API | getAttachments(): ?array | setAttachments(?array attachments): void |
| `brandingThemeID` | `?string` | Optional | See BrandingThemes | getBrandingThemeID(): ?string | setBrandingThemeID(?string brandingThemeID): void |
| `cISDeduction` | `?float` | Optional, Read-only | CIS deduction for UK contractors | getCISDeduction(): ?float | setCISDeduction(?float cISDeduction): void |
| `cISRate` | `?float` | Optional, Read-only | CIS Deduction rate for the organisation | getCISRate(): ?float | setCISRate(?float cISRate): void |
| `contact` | [`?Contact`](../../doc/models/contact.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/) | getContact(): ?Contact | setContact(?Contact contact): void |
| `creditNotes` | [`?(CreditNote[])`](../../doc/models/credit-note.md) | Optional, Read-only | Details of credit notes that have been applied to an invoice | getCreditNotes(): ?array | setCreditNotes(?array creditNotes): void |
| `currencyCode` | [`?string(CurrencyCodeEnum)`](../../doc/models/currency-code-enum.md) | Optional | 3 letter alpha code for the currency – see list of currency codes | getCurrencyCode(): ?string | setCurrencyCode(?string currencyCode): void |
| `currencyRate` | `?float` | Optional | The currency rate for a multicurrency invoice. If no rate is specified, the XE.com day rate is used. (max length = [18].[6]) | getCurrencyRate(): ?float | setCurrencyRate(?float currencyRate): void |
| `date` | `?string` | Optional | Date invoice was issued – YYYY-MM-DD. If the Date element is not specified it will default to the current date based on the timezone setting of the organisation | getDate(): ?string | setDate(?string date): void |
| `dueDate` | `?string` | Optional | Date invoice is due – YYYY-MM-DD | getDueDate(): ?string | setDueDate(?string dueDate): void |
| `expectedPaymentDate` | `?string` | Optional | Shown on sales invoices (Accounts Receivable) when this has been set | getExpectedPaymentDate(): ?string | setExpectedPaymentDate(?string expectedPaymentDate): void |
| `fullyPaidOnDate` | `?string` | Optional, Read-only | The date the invoice was fully paid. Only returned on fully paid invoices | getFullyPaidOnDate(): ?string | setFullyPaidOnDate(?string fullyPaidOnDate): void |
| `hasAttachments` | `?bool` | Optional, Read-only | boolean to indicate if an invoice has an attachment<br><br>**Default**: `false` | getHasAttachments(): ?bool | setHasAttachments(?bool hasAttachments): void |
| `hasErrors` | `?bool` | Optional | A boolean to indicate if a invoice has an validation errors<br><br>**Default**: `false` | getHasErrors(): ?bool | setHasErrors(?bool hasErrors): void |
| `invoiceID` | `?string` | Optional | Xero generated unique identifier for invoice | getInvoiceID(): ?string | setInvoiceID(?string invoiceID): void |
| `invoiceNumber` | `?string` | Optional | ACCREC – Unique alpha numeric code identifying invoice (when missing will auto-generate from your Organisation Invoice Settings) (max length = 255)<br><br>**Constraints**: *Maximum Length*: `255` | getInvoiceNumber(): ?string | setInvoiceNumber(?string invoiceNumber): void |
| `isDiscounted` | `?bool` | Optional, Read-only | boolean to indicate if an invoice has a discount | getIsDiscounted(): ?bool | setIsDiscounted(?bool isDiscounted): void |
| `lineAmountTypes` | [`?string(LineAmountTypesEnum)`](../../doc/models/line-amount-types-enum.md) | Optional | Line amounts are exclusive of tax by default if you don’t specify this element. See Line Amount Types | getLineAmountTypes(): ?string | setLineAmountTypes(?string lineAmountTypes): void |
| `lineItems` | [`?(LineItem[])`](../../doc/models/line-item.md) | Optional | See LineItems | getLineItems(): ?array | setLineItems(?array lineItems): void |
| `overpayments` | [`?(Overpayment[])`](../../doc/models/overpayment.md) | Optional, Read-only | See Overpayments | getOverpayments(): ?array | setOverpayments(?array overpayments): void |
| `payments` | [`?(Payment[])`](../../doc/models/payment.md) | Optional, Read-only | See Payments | getPayments(): ?array | setPayments(?array payments): void |
| `plannedPaymentDate` | `?string` | Optional | Shown on bills (Accounts Payable) when this has been set | getPlannedPaymentDate(): ?string | setPlannedPaymentDate(?string plannedPaymentDate): void |
| `prepayments` | [`?(Prepayment[])`](../../doc/models/prepayment.md) | Optional, Read-only | See Prepayments | getPrepayments(): ?array | setPrepayments(?array prepayments): void |
| `reference` | `?string` | Optional | ACCREC only – additional reference number | getReference(): ?string | setReference(?string reference): void |
| `repeatingInvoiceID` | `?string` | Optional | Xero generated unique identifier for repeating invoices | getRepeatingInvoiceID(): ?string | setRepeatingInvoiceID(?string repeatingInvoiceID): void |
| `sentToContact` | `?bool` | Optional | Boolean to set whether the invoice in the Xero app should be marked as “sent”. This can be set only on invoices that have been approved | getSentToContact(): ?bool | setSentToContact(?bool sentToContact): void |
| `status` | [`?string(Status5Enum)`](../../doc/models/status-5-enum.md) | Optional | See Invoice Status Codes | getStatus(): ?string | setStatus(?string status): void |
| `statusAttributeString` | `?string` | Optional | A string to indicate if a invoice status | getStatusAttributeString(): ?string | setStatusAttributeString(?string statusAttributeString): void |
| `subTotal` | `?float` | Optional, Read-only | Total of invoice excluding taxes | getSubTotal(): ?float | setSubTotal(?float subTotal): void |
| `total` | `?float` | Optional, Read-only | Total of Invoice tax inclusive (i.e. SubTotal + TotalTax). This will be ignored if it doesn’t equal the sum of the LineAmounts | getTotal(): ?float | setTotal(?float total): void |
| `totalDiscount` | `?float` | Optional, Read-only | Total of discounts applied on the invoice line items | getTotalDiscount(): ?float | setTotalDiscount(?float totalDiscount): void |
| `totalTax` | `?float` | Optional, Read-only | Total tax on invoice | getTotalTax(): ?float | setTotalTax(?float totalTax): void |
| `type` | [`?string(Type3Enum)`](../../doc/models/type-3-enum.md) | Optional | See Invoice Types | getType(): ?string | setType(?string type): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | Last modified date UTC format | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `url` | `?string` | Optional | URL link to a source document – shown as “Go to [appName]” in the Xero app | getUrl(): ?string | setUrl(?string url): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |
| `warnings` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of warning messages from the API | getWarnings(): ?array | setWarnings(?array warnings): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\InvoiceBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;

$invoice = InvoiceBuilder::init()
    ->amountCredited(67.76)
    ->amountDue(132.18)
    ->amountPaid(62.02)
    ->attachments(
        [
            AttachmentBuilder::init()
                ->attachmentID('00000714-0000-0000-0000-000000000000')
                ->contentLength(34)
                ->fileName('FileName6')
                ->includeOnline(false)
                ->mimeType('MimeType6')
                ->build()
        ]
    )
    ->brandingThemeID('00000176-0000-0000-0000-000000000000')
    ->hasAttachments(false)
    ->hasErrors(false)
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

