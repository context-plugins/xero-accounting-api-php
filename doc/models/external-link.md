
# External Link

Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/)

## Structure

`ExternalLink`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | - | getDescription(): ?string | setDescription(?string description): void |
| `linkType` | [`?string(LinkTypeEnum)`](../../doc/models/link-type-enum.md) | Optional | See External link types | getLinkType(): ?string | setLinkType(?string linkType): void |
| `url` | `?string` | Optional | URL for service e.g. http://twitter.com/xeroapi | getUrl(): ?string | setUrl(?string url): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ExternalLinkBuilder;
use XeroAccountingAPILib\Models\LinkTypeEnum;

$externalLink = ExternalLinkBuilder::init()
    ->description('Description0')
    ->linkType(LinkTypeEnum::GOOGLEPLUS)
    ->url('Url6')
    ->build();
```

