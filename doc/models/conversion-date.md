
# Conversion Date

The date when the organisation starts using Xero

## Structure

`ConversionDate`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `month` | `?int` | Optional | The month the organisation starts using Xero. Value is an integer between 1 and 12 | getMonth(): ?int | setMonth(?int month): void |
| `year` | `?int` | Optional | The year the organisation starts using Xero. Value is an integer greater than 2006 | getYear(): ?int | setYear(?int year): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ConversionDateBuilder;

$conversionDate = ConversionDateBuilder::init()
    ->month(1)
    ->year(2020)
    ->build();
```

