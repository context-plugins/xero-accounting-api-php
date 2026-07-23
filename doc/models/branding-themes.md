
# Branding Themes

## Structure

`BrandingThemes`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `brandingThemes` | [`?(BrandingTheme[])`](../../doc/models/branding-theme.md) | Optional | - | getBrandingThemes(): ?array | setBrandingThemes(?array brandingThemes): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\BrandingThemesBuilder;
use XeroAccountingAPILib\Models\Builders\BrandingThemeBuilder;

$brandingThemes = BrandingThemesBuilder::init()
    ->brandingThemes(
        [
            BrandingThemeBuilder::init()
                ->brandingThemeID('00001a68-0000-0000-0000-000000000000')
                ->createdDateUTC('CreatedDateUTC8')
                ->logoUrl('LogoUrl6')
                ->name('Name0')
                ->sortOrder(118)
                ->build()
        ]
    )
    ->build();
```

