
# CIS Settings

## Structure

`CISSettings`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cISSettings` | [`?(CISSetting[])`](../../doc/models/cis-setting.md) | Optional | - | getCISSettings(): ?array | setCISSettings(?array cISSettings): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\CISSettingsBuilder;
use XeroAccountingAPILib\Models\Builders\CISSettingBuilder;

$cISSettings = CISSettingsBuilder::init()
    ->cISSettings(
        [
            CISSettingBuilder::init()
                ->cISEnabled(false)
                ->rate(65.2)
                ->build(),
            CISSettingBuilder::init()
                ->cISEnabled(false)
                ->rate(65.2)
                ->build()
        ]
    )
    ->build();
```

