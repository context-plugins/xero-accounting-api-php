
# Report

Find out more here: [http://developer.xero.com/documentation/api/reports/](http://developer.xero.com/documentation/api/reports/)

## Structure

`Report`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `contacts` | [`?(TenNinetyNineContact[])`](../../doc/models/ten-ninety-nine-contact.md) | Optional | - | getContacts(): ?array | setContacts(?array contacts): void |
| `reportDate` | `?string` | Optional | Date of report | getReportDate(): ?string | setReportDate(?string reportDate): void |
| `reportID` | `?string` | Optional | See Prepayment Types | getReportID(): ?string | setReportID(?string reportID): void |
| `reportName` | `?string` | Optional | See Prepayment Types | getReportName(): ?string | setReportName(?string reportName): void |
| `reportTitle` | `?string` | Optional | See Prepayment Types | getReportTitle(): ?string | setReportTitle(?string reportTitle): void |
| `reportType` | [`?string(ReportTypeEnum)`](../../doc/models/report-type-enum.md) | Optional | See Prepayment Types | getReportType(): ?string | setReportType(?string reportType): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | Updated Date | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ReportBuilder;
use XeroAccountingAPILib\Models\Builders\TenNinetyNineContactBuilder;

$report = ReportBuilder::init()
    ->contacts(
        [
            TenNinetyNineContactBuilder::init()
                ->box1(165.98)
                ->box10(51.22)
                ->box11(1.58)
                ->box13(175.52)
                ->box14(72.92)
                ->build()
        ]
    )
    ->reportDate('ReportDate2')
    ->reportID('ReportID8')
    ->reportName('ReportName8')
    ->reportTitle('ReportTitle4')
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

