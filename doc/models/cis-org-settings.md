
# CIS Org Settings

## Structure

`CISOrgSettings`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cISSettings` | [`?(CISOrgSetting[])`](../../doc/models/cis-org-setting.md) | Optional | - | getCISSettings(): ?array | setCISSettings(?array cISSettings): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\CISOrgSettingsBuilder;
use XeroAccountingAPILib\Models\Builders\CISOrgSettingBuilder;

$cISOrgSettings = CISOrgSettingsBuilder::init()
    ->cISSettings(
        [
            CISOrgSettingBuilder::init()
                ->cISContractorEnabled(false)
                ->cISSubContractorEnabled(false)
                ->rate(65.2)
                ->build(),
            CISOrgSettingBuilder::init()
                ->cISContractorEnabled(false)
                ->cISSubContractorEnabled(false)
                ->rate(65.2)
                ->build()
        ]
    )
    ->build();
```

