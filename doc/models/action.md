
# Action

Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/)

## Structure

`Action`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | Name of the actions for this organisation | getName(): ?string | setName(?string name): void |
| `status` | [`?string(Status1Enum)`](../../doc/models/status-1-enum.md) | Optional | Status of the action for this organisation | getStatus(): ?string | setStatus(?string status): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ActionBuilder;
use XeroAccountingAPILib\Models\Status1Enum;

$action = ActionBuilder::init()
    ->name('UseMulticurrency')
    ->status(Status1Enum::ALLOWED)
    ->build();
```

