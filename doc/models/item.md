
# Item

Find out more here: [http://developer.xero.com/documentation/api/items/](http://developer.xero.com/documentation/api/items/)

## Structure

`Item`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `code` | `string` | Required | User defined item code (max length = 30)<br><br>**Constraints**: *Maximum Length*: `30` | getCode(): string | setCode(string code): void |
| `description` | `?string` | Optional | The sales description of the item (max length = 4000)<br><br>**Constraints**: *Maximum Length*: `4000` | getDescription(): ?string | setDescription(?string description): void |
| `inventoryAssetAccountCode` | `?string` | Optional | The inventory asset account for the item. The account must be of type INVENTORY. The  COGSAccountCode in PurchaseDetails is also required to create a tracked item | getInventoryAssetAccountCode(): ?string | setInventoryAssetAccountCode(?string inventoryAssetAccountCode): void |
| `isPurchased` | `?bool` | Optional | Boolean value, defaults to true. When IsPurchased is true the item is available for purchase transactions in the Xero UI. If IsPurchased is updated to false then PurchaseDescription and PurchaseDetails values will be nulled. | getIsPurchased(): ?bool | setIsPurchased(?bool isPurchased): void |
| `isSold` | `?bool` | Optional | Boolean value, defaults to true. When IsSold is true the item will be available on sales transactions in the Xero UI. If IsSold is updated to false then Description and SalesDetails values will be nulled. | getIsSold(): ?bool | setIsSold(?bool isSold): void |
| `isTrackedAsInventory` | `?bool` | Optional | True for items that are tracked as inventory. An item will be tracked as inventory if the InventoryAssetAccountCode and COGSAccountCode are set. | getIsTrackedAsInventory(): ?bool | setIsTrackedAsInventory(?bool isTrackedAsInventory): void |
| `itemID` | `?string` | Optional | The Xero identifier for an Item | getItemID(): ?string | setItemID(?string itemID): void |
| `name` | `?string` | Optional | The name of the item (max length = 50)<br><br>**Constraints**: *Maximum Length*: `50` | getName(): ?string | setName(?string name): void |
| `purchaseDescription` | `?string` | Optional | The purchase description of the item (max length = 4000)<br><br>**Constraints**: *Maximum Length*: `4000` | getPurchaseDescription(): ?string | setPurchaseDescription(?string purchaseDescription): void |
| `purchaseDetails` | [`?Purchase`](../../doc/models/purchase.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/items/](http://developer.xero.com/documentation/api/items/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/items/](http://developer.xero.com/documentation/api/items/) | getPurchaseDetails(): ?Purchase | setPurchaseDetails(?Purchase purchaseDetails): void |
| `quantityOnHand` | `?float` | Optional | The quantity of the item on hand | getQuantityOnHand(): ?float | setQuantityOnHand(?float quantityOnHand): void |
| `salesDetails` | [`?Purchase`](../../doc/models/purchase.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/items/](http://developer.xero.com/documentation/api/items/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/items/](http://developer.xero.com/documentation/api/items/) | getSalesDetails(): ?Purchase | setSalesDetails(?Purchase salesDetails): void |
| `statusAttributeString` | `?string` | Optional | Status of object | getStatusAttributeString(): ?string | setStatusAttributeString(?string statusAttributeString): void |
| `totalCostPool` | `?float` | Optional | The value of the item on hand. Calculated using average cost accounting. | getTotalCostPool(): ?float | setTotalCostPool(?float totalCostPool): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | Last modified date in UTC format | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays array of validation error messages from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ItemBuilder;

$item = ItemBuilder::init(
    'Code2'
)
    ->description('Description6')
    ->inventoryAssetAccountCode('InventoryAssetAccountCode8')
    ->isPurchased(false)
    ->isSold(false)
    ->isTrackedAsInventory(false)
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

