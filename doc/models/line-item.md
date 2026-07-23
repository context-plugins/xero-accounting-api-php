
# Line Item

Find out more here: [https://developer.xero.com/documentation/api/invoices#post](https://developer.xero.com/documentation/api/invoices#post)

## Structure

`LineItem`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountCode` | `?string` | Optional | See Accounts | getAccountCode(): ?string | setAccountCode(?string accountCode): void |
| `description` | `?string` | Optional | Description needs to be at least 1 char long. A line item with just a description (i.e no unit amount or quantity) can be created by specifying just a <Description> element that contains at least 1 character | getDescription(): ?string | setDescription(?string description): void |
| `discountAmount` | `?float` | Optional | Discount amount being applied to a line item. Only supported on ACCREC invoices - ACCPAY invoices and credit notes in Xero do not support discounts. | getDiscountAmount(): ?float | setDiscountAmount(?float discountAmount): void |
| `discountRate` | `?float` | Optional | Percentage discount being applied to a line item (only supported on  ACCREC invoices – ACC PAY invoices and credit notes in Xero do not support discounts | getDiscountRate(): ?float | setDiscountRate(?float discountRate): void |
| `itemCode` | `?string` | Optional | See Items | getItemCode(): ?string | setItemCode(?string itemCode): void |
| `lineAmount` | `?float` | Optional | If you wish to omit either of the <Quantity> or <UnitAmount> you can provide a LineAmount and Xero will calculate the missing amount for you. The line amount reflects the discounted price if a DiscountRate has been used . i.e LineAmount = Quantity * Unit Amount * ((100 – DiscountRate)/100) | getLineAmount(): ?float | setLineAmount(?float lineAmount): void |
| `lineItemID` | `?string` | Optional | LineItem unique ID | getLineItemID(): ?string | setLineItemID(?string lineItemID): void |
| `quantity` | `?float` | Optional | LineItem Quantity | getQuantity(): ?float | setQuantity(?float quantity): void |
| `repeatingInvoiceID` | `?string` | Optional | The Xero identifier for a Repeating Invoice | getRepeatingInvoiceID(): ?string | setRepeatingInvoiceID(?string repeatingInvoiceID): void |
| `taxAmount` | `?float` | Optional | The tax amount is auto calculated as a percentage of the line amount (see below) based on the tax rate. This value can be overriden if the calculated <TaxAmount> is not correct. | getTaxAmount(): ?float | setTaxAmount(?float taxAmount): void |
| `taxType` | `?string` | Optional | The tax type from TaxRates | getTaxType(): ?string | setTaxType(?string taxType): void |
| `tracking` | [`?(LineItemTracking[])`](../../doc/models/line-item-tracking.md) | Optional | Optional Tracking Category – see Tracking.  Any LineItem can have a  maximum of 2 <TrackingCategory> elements. | getTracking(): ?array | setTracking(?array tracking): void |
| `unitAmount` | `?float` | Optional | LineItem Unit Amount | getUnitAmount(): ?float | setUnitAmount(?float unitAmount): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\LineItemBuilder;

$lineItem = LineItemBuilder::init()
    ->accountCode('AccountCode0')
    ->description('Description0')
    ->discountAmount(57.42)
    ->discountRate(157.2)
    ->itemCode('ItemCode6')
    ->lineItemID('00000000-0000-0000-0000-000000000000')
    ->repeatingInvoiceID('00000000-0000-0000-0000-000000000000')
    ->build();
```

