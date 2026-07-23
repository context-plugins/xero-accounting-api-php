
# Report Row

## Structure

`ReportRow`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cells` | [`?(ReportCell[])`](../../doc/models/report-cell.md) | Optional | - | getCells(): ?array | setCells(?array cells): void |
| `rowType` | [`?string(RowTypeEnum)`](../../doc/models/row-type-enum.md) | Optional | - | getRowType(): ?string | setRowType(?string rowType): void |
| `title` | `?string` | Optional | - | getTitle(): ?string | setTitle(?string title): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ReportRowBuilder;
use XeroAccountingAPILib\Models\Builders\ReportCellBuilder;
use XeroAccountingAPILib\Models\Builders\ReportAttributeBuilder;
use XeroAccountingAPILib\Models\RowTypeEnum;

$reportRow = ReportRowBuilder::init()
    ->cells(
        [
            ReportCellBuilder::init()
                ->attributes(
                    [
                        ReportAttributeBuilder::init()
                            ->id('Id4')
                            ->value('Value6')
                            ->build(),
                        ReportAttributeBuilder::init()
                            ->id('Id4')
                            ->value('Value6')
                            ->build(),
                        ReportAttributeBuilder::init()
                            ->id('Id4')
                            ->value('Value6')
                            ->build()
                    ]
                )
                ->value('Value0')
                ->build(),
            ReportCellBuilder::init()
                ->attributes(
                    [
                        ReportAttributeBuilder::init()
                            ->id('Id4')
                            ->value('Value6')
                            ->build(),
                        ReportAttributeBuilder::init()
                            ->id('Id4')
                            ->value('Value6')
                            ->build(),
                        ReportAttributeBuilder::init()
                            ->id('Id4')
                            ->value('Value6')
                            ->build()
                    ]
                )
                ->value('Value0')
                ->build()
        ]
    )
    ->rowType(RowTypeEnum::ROW)
    ->title('Title4')
    ->build();
```

