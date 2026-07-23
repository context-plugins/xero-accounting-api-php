
# Report with Rows

## Structure

`ReportWithRows`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `reports` | [`?(ReportWithRow[])`](../../doc/models/report-with-row.md) | Optional | - | getReports(): ?array | setReports(?array reports): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ReportWithRowsBuilder;
use XeroAccountingAPILib\Models\Builders\ReportWithRowBuilder;
use XeroAccountingAPILib\Models\Builders\ReportFieldsBuilder;

$reportWithRows = ReportWithRowsBuilder::init()
    ->reports(
        [
            ReportWithRowBuilder::init()
                ->fields(
                    [
                        ReportFieldsBuilder::init()
                            ->description('Description6')
                            ->fieldID('FieldID8')
                            ->value('Value2')
                            ->build()
                    ]
                )
                ->reportDate('ReportDate6')
                ->reportID('ReportID2')
                ->reportName('ReportName8')
                ->reportTitle('ReportTitle8')
                ->build(),
            ReportWithRowBuilder::init()
                ->fields(
                    [
                        ReportFieldsBuilder::init()
                            ->description('Description6')
                            ->fieldID('FieldID8')
                            ->value('Value2')
                            ->build()
                    ]
                )
                ->reportDate('ReportDate6')
                ->reportID('ReportID2')
                ->reportName('ReportName8')
                ->reportTitle('ReportTitle8')
                ->build()
        ]
    )
    ->build();
```

