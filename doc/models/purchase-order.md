
# Purchase Order

Find out more here: [http://developer.xero.com/documentation/api/purchase-orders/](http://developer.xero.com/documentation/api/purchase-orders/)

## Structure

`PurchaseOrder`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `attachments` | [`?(Attachment[])`](../../doc/models/attachment.md) | Optional | Displays array of attachments from the API | getAttachments(): ?array | setAttachments(?array attachments): void |
| `attentionTo` | `?string` | Optional | The person that the delivery is going to | getAttentionTo(): ?string | setAttentionTo(?string attentionTo): void |
| `brandingThemeID` | `?string` | Optional | See BrandingThemes | getBrandingThemeID(): ?string | setBrandingThemeID(?string brandingThemeID): void |
| `contact` | [`?Contact`](../../doc/models/contact.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/) | getContact(): ?Contact | setContact(?Contact contact): void |
| `currencyCode` | [`?string(CurrencyCodeEnum)`](../../doc/models/currency-code-enum.md) | Optional | 3 letter alpha code for the currency – see list of currency codes | getCurrencyCode(): ?string | setCurrencyCode(?string currencyCode): void |
| `currencyRate` | `?float` | Optional | The currency rate for a multicurrency purchase order. If no rate is specified, the XE.com day rate is used. | getCurrencyRate(): ?float | setCurrencyRate(?float currencyRate): void |
| `date` | `?string` | Optional | Date purchase order was issued – YYYY-MM-DD. If the Date element is not specified then it will default to the current date based on the timezone setting of the organisation | getDate(): ?string | setDate(?string date): void |
| `deliveryAddress` | `?string` | Optional | The address the goods are to be delivered to | getDeliveryAddress(): ?string | setDeliveryAddress(?string deliveryAddress): void |
| `deliveryDate` | `?string` | Optional | Date the goods are to be delivered – YYYY-MM-DD | getDeliveryDate(): ?string | setDeliveryDate(?string deliveryDate): void |
| `deliveryInstructions` | `?string` | Optional | A free text feild for instructions (500 characters max) | getDeliveryInstructions(): ?string | setDeliveryInstructions(?string deliveryInstructions): void |
| `expectedArrivalDate` | `?string` | Optional | The date the goods are expected to arrive. | getExpectedArrivalDate(): ?string | setExpectedArrivalDate(?string expectedArrivalDate): void |
| `hasAttachments` | `?bool` | Optional, Read-only | boolean to indicate if a purchase order has an attachment<br><br>**Default**: `false` | getHasAttachments(): ?bool | setHasAttachments(?bool hasAttachments): void |
| `lineAmountTypes` | [`?string(LineAmountTypesEnum)`](../../doc/models/line-amount-types-enum.md) | Optional | Line amounts are exclusive of tax by default if you don’t specify this element. See Line Amount Types | getLineAmountTypes(): ?string | setLineAmountTypes(?string lineAmountTypes): void |
| `lineItems` | [`?(LineItem[])`](../../doc/models/line-item.md) | Optional | See LineItems | getLineItems(): ?array | setLineItems(?array lineItems): void |
| `purchaseOrderID` | `?string` | Optional | Xero generated unique identifier for purchase order | getPurchaseOrderID(): ?string | setPurchaseOrderID(?string purchaseOrderID): void |
| `purchaseOrderNumber` | `?string` | Optional | Unique alpha numeric code identifying purchase order (when missing will auto-generate from your Organisation Invoice Settings) | getPurchaseOrderNumber(): ?string | setPurchaseOrderNumber(?string purchaseOrderNumber): void |
| `reference` | `?string` | Optional | Additional reference number | getReference(): ?string | setReference(?string reference): void |
| `sentToContact` | `?bool` | Optional | Boolean to set whether the purchase order should be marked as “sent”. This can be set only on purchase orders that have been approved or billed | getSentToContact(): ?bool | setSentToContact(?bool sentToContact): void |
| `status` | [`?string(Status17Enum)`](../../doc/models/status-17-enum.md) | Optional | See Purchase Order Status Codes | getStatus(): ?string | setStatus(?string status): void |
| `statusAttributeString` | `?string` | Optional | A string to indicate if a invoice status | getStatusAttributeString(): ?string | setStatusAttributeString(?string statusAttributeString): void |
| `subTotal` | `?float` | Optional, Read-only | Total of purchase order excluding taxes | getSubTotal(): ?float | setSubTotal(?float subTotal): void |
| `telephone` | `?string` | Optional | The phone number for the person accepting the delivery | getTelephone(): ?string | setTelephone(?string telephone): void |
| `total` | `?float` | Optional, Read-only | Total of Purchase Order tax inclusive (i.e. SubTotal + TotalTax) | getTotal(): ?float | setTotal(?float total): void |
| `totalDiscount` | `?float` | Optional, Read-only | Total of discounts applied on the purchase order line items | getTotalDiscount(): ?float | setTotalDiscount(?float totalDiscount): void |
| `totalTax` | `?float` | Optional, Read-only | Total tax on purchase order | getTotalTax(): ?float | setTotalTax(?float totalTax): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | Last modified date UTC format | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |
| `warnings` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of warning messages from the API | getWarnings(): ?array | setWarnings(?array warnings): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\PurchaseOrderBuilder;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;

$purchaseOrder = PurchaseOrderBuilder::init()
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
    ->attentionTo('AttentionTo0')
    ->brandingThemeID('0000007a-0000-0000-0000-000000000000')
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
    ->currencyCode(CurrencyCodeEnum::NIO)
    ->hasAttachments(false)
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

