
# Reports

## Structure

`Reports`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `reports` | [`?(Report[])`](../../doc/models/report.md) | Optional | - | getReports(): ?array | setReports(?array reports): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ReportsBuilder;
use XeroAccountingAPILib\Models\Builders\ReportBuilder;
use XeroAccountingAPILib\Models\Builders\TenNinetyNineContactBuilder;

$reports = ReportsBuilder::init()
    ->reports(
        [
            ReportBuilder::init()
                ->contacts(
                    [
                        TenNinetyNineContactBuilder::init()
                            ->box1(165.98)
                            ->box10(51.22)
                            ->box11(1.58)
                            ->box13(175.52)
                            ->box14(72.92)
                            ->build(),
                        TenNinetyNineContactBuilder::init()
                            ->box1(165.98)
                            ->box10(51.22)
                            ->box11(1.58)
                            ->box13(175.52)
                            ->box14(72.92)
                            ->build(),
                        TenNinetyNineContactBuilder::init()
                            ->box1(165.98)
                            ->box10(51.22)
                            ->box11(1.58)
                            ->box13(175.52)
                            ->box14(72.92)
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

