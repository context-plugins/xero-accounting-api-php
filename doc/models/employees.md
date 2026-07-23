
# Employees

## Structure

`Employees`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `employees` | [`?(Employee[])`](../../doc/models/employee.md) | Optional | - | getEmployees(): ?array | setEmployees(?array employees): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\EmployeesBuilder;
use XeroAccountingAPILib\Models\Builders\EmployeeBuilder;
use XeroAccountingAPILib\Models\Builders\ExternalLinkBuilder;
use XeroAccountingAPILib\Models\LinkTypeEnum;
use XeroAccountingAPILib\Models\Status10Enum;

$employees = EmployeesBuilder::init()
    ->employees(
        [
            EmployeeBuilder::init()
                ->employeeID('000009cc-0000-0000-0000-000000000000')
                ->externalLink(
                    ExternalLinkBuilder::init()
                        ->description('Description8')
                        ->linkType(LinkTypeEnum::TWITTER)
                        ->url('Url4')
                        ->build()
                )
                ->firstName('FirstName8')
                ->lastName('LastName8')
                ->status(Status10Enum::GDPRREQUEST)
                ->build()
        ]
    )
    ->build();
```

