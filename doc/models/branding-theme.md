
# Branding Theme

Find out more here: [http://developer.xero.com/documentation/api/branding-themes/](http://developer.xero.com/documentation/api/branding-themes/)

## Structure

`BrandingTheme`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `brandingThemeID` | `?string` | Optional | Xero identifier | getBrandingThemeID(): ?string | setBrandingThemeID(?string brandingThemeID): void |
| `createdDateUTC` | `?string` | Optional, Read-only | UTC timestamp of creation date of branding theme | getCreatedDateUTC(): ?string | setCreatedDateUTC(?string createdDateUTC): void |
| `logoUrl` | `?string` | Optional | The location of the image file used as the logo on this branding theme | getLogoUrl(): ?string | setLogoUrl(?string logoUrl): void |
| `name` | `?string` | Optional | Name of branding theme | getName(): ?string | setName(?string name): void |
| `sortOrder` | `?int` | Optional | Integer – ranked order of branding theme. The default branding theme has a value of 0 | getSortOrder(): ?int | setSortOrder(?int sortOrder): void |
| `type` | [`?string(TypeEnum)`](../../doc/models/type-enum.md) | Optional | Always INVOICE | getType(): ?string | setType(?string type): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\BrandingThemeBuilder;

$brandingTheme = BrandingThemeBuilder::init()
    ->brandingThemeID('000014b4-0000-0000-0000-000000000000')
    ->createdDateUTC('/Date(1573755038314)/')
    ->logoUrl('LogoUrl6')
    ->name('Name0')
    ->sortOrder(26)
    ->build();
```

