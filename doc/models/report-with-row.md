
# Report with Row

Find out more here: [http://developer.xero.com/documentation/api/reports/](http://developer.xero.com/documentation/api/reports/)

## Structure

`ReportWithRow`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `fields` | [`?(ReportFields[])`](../../doc/models/report-fields.md) | Optional | - | getFields(): ?array | setFields(?array fields): void |
| `reportDate` | `?string` | Optional | Date of report | getReportDate(): ?string | setReportDate(?string reportDate): void |
| `reportID` | `?string` | Optional | Report id | getReportID(): ?string | setReportID(?string reportID): void |
| `reportName` | `?string` | Optional | Name of the report | getReportName(): ?string | setReportName(?string reportName): void |
| `reportTitle` | `?string` | Optional | Title of the report | getReportTitle(): ?string | setReportTitle(?string reportTitle): void |
| `reportTitles` | `?(string[])` | Optional | Report titles array (3 to 4 strings with the report name, orgnisation name and time frame of report) | getReportTitles(): ?array | setReportTitles(?array reportTitles): void |
| `reportType` | `?string` | Optional | The type of report (BalanceSheet,ProfitLoss, etc) | getReportType(): ?string | setReportType(?string reportType): void |
| `rows` | [`?(ReportRows[])`](../../doc/models/report-rows.md) | Optional | - | getRows(): ?array | setRows(?array rows): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | Updated Date | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ReportWithRowBuilder;
use XeroAccountingAPILib\Models\Builders\ReportFieldsBuilder;

$reportWithRow = ReportWithRowBuilder::init()
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
    ->reportName('ReportName2')
    ->reportTitle('ReportTitle8')
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

