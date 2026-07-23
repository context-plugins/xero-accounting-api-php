
# Tracking Categories

## Structure

`TrackingCategories`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `trackingCategories` | [`?(TrackingCategory[])`](../../doc/models/tracking-category.md) | Optional | - | getTrackingCategories(): ?array | setTrackingCategories(?array trackingCategories): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\TrackingCategoriesBuilder;
use XeroAccountingAPILib\Models\Builders\TrackingCategoryBuilder;
use XeroAccountingAPILib\Models\Builders\TrackingOptionBuilder;
use XeroAccountingAPILib\Models\Status13Enum;
use XeroAccountingAPILib\Models\Status14Enum;

$trackingCategories = TrackingCategoriesBuilder::init()
    ->trackingCategories(
        [
            TrackingCategoryBuilder::init()
                ->name('Name6')
                ->option('Option4')
                ->options(
                    [
                        TrackingOptionBuilder::init()
                            ->name('Name2')
                            ->status(Status13Enum::ARCHIVED)
                            ->trackingCategoryID('00000ecc-0000-0000-0000-000000000000')
                            ->trackingOptionID('000009c8-0000-0000-0000-000000000000')
                            ->build(),
                        TrackingOptionBuilder::init()
                            ->name('Name2')
                            ->status(Status13Enum::ARCHIVED)
                            ->trackingCategoryID('00000ecc-0000-0000-0000-000000000000')
                            ->trackingOptionID('000009c8-0000-0000-0000-000000000000')
                            ->build()
                    ]
                )
                ->status(Status14Enum::ACTIVE)
                ->trackingCategoryID('0000262a-0000-0000-0000-000000000000')
                ->build(),
            TrackingCategoryBuilder::init()
                ->name('Name6')
                ->option('Option4')
                ->options(
                    [
                        TrackingOptionBuilder::init()
                            ->name('Name2')
                            ->status(Status13Enum::ARCHIVED)
                            ->trackingCategoryID('00000ecc-0000-0000-0000-000000000000')
                            ->trackingOptionID('000009c8-0000-0000-0000-000000000000')
                            ->build(),
                        TrackingOptionBuilder::init()
                            ->name('Name2')
                            ->status(Status13Enum::ARCHIVED)
                            ->trackingCategoryID('00000ecc-0000-0000-0000-000000000000')
                            ->trackingOptionID('000009c8-0000-0000-0000-000000000000')
                            ->build()
                    ]
                )
                ->status(Status14Enum::ACTIVE)
                ->trackingCategoryID('0000262a-0000-0000-0000-000000000000')
                ->build(),
            TrackingCategoryBuilder::init()
                ->name('Name6')
                ->option('Option4')
                ->options(
                    [
                        TrackingOptionBuilder::init()
                            ->name('Name2')
                            ->status(Status13Enum::ARCHIVED)
                            ->trackingCategoryID('00000ecc-0000-0000-0000-000000000000')
                            ->trackingOptionID('000009c8-0000-0000-0000-000000000000')
                            ->build(),
                        TrackingOptionBuilder::init()
                            ->name('Name2')
                            ->status(Status13Enum::ARCHIVED)
                            ->trackingCategoryID('00000ecc-0000-0000-0000-000000000000')
                            ->trackingOptionID('000009c8-0000-0000-0000-000000000000')
                            ->build()
                    ]
                )
                ->status(Status14Enum::ACTIVE)
                ->trackingCategoryID('0000262a-0000-0000-0000-000000000000')
                ->build()
        ]
    )
    ->build();
```

