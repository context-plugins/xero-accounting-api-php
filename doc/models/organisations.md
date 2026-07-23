
# Organisations

## Structure

`Organisations`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `organisations` | [`?(Organisation[])`](../../doc/models/organisation.md) | Optional | - | getOrganisations(): ?array | setOrganisations(?array organisations): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\OrganisationsBuilder;
use XeroAccountingAPILib\Models\Builders\OrganisationBuilder;
use XeroAccountingAPILib\Models\Builders\AddressForOrganisationBuilder;
use XeroAccountingAPILib\Models\AddressType1Enum;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;
use XeroAccountingAPILib\Models\Class1Enum;
use XeroAccountingAPILib\Models\CountryCodeEnum;

$organisations = OrganisationsBuilder::init()
    ->organisations(
        [
            OrganisationBuilder::init()
                ->aPIKey('APIKey4')
                ->addresses(
                    [
                        AddressForOrganisationBuilder::init()
                            ->addressLine1('AddressLine14')
                            ->addressLine2('AddressLine20')
                            ->addressLine3('AddressLine38')
                            ->addressLine4('AddressLine46')
                            ->addressType(AddressType1Enum::DELIVERY)
                            ->build(),
                        AddressForOrganisationBuilder::init()
                            ->addressLine1('AddressLine14')
                            ->addressLine2('AddressLine20')
                            ->addressLine3('AddressLine38')
                            ->addressLine4('AddressLine46')
                            ->addressType(AddressType1Enum::DELIVERY)
                            ->build(),
                        AddressForOrganisationBuilder::init()
                            ->addressLine1('AddressLine14')
                            ->addressLine2('AddressLine20')
                            ->addressLine3('AddressLine38')
                            ->addressLine4('AddressLine46')
                            ->addressType(AddressType1Enum::DELIVERY)
                            ->build()
                    ]
                )
                ->baseCurrency(CurrencyCodeEnum::BND)
                ->class(Class1Enum::NON_GST_CASHBOOK)
                ->countryCode(CountryCodeEnum::PN)
                ->build(),
            OrganisationBuilder::init()
                ->aPIKey('APIKey4')
                ->addresses(
                    [
                        AddressForOrganisationBuilder::init()
                            ->addressLine1('AddressLine14')
                            ->addressLine2('AddressLine20')
                            ->addressLine3('AddressLine38')
                            ->addressLine4('AddressLine46')
                            ->addressType(AddressType1Enum::DELIVERY)
                            ->build(),
                        AddressForOrganisationBuilder::init()
                            ->addressLine1('AddressLine14')
                            ->addressLine2('AddressLine20')
                            ->addressLine3('AddressLine38')
                            ->addressLine4('AddressLine46')
                            ->addressType(AddressType1Enum::DELIVERY)
                            ->build(),
                        AddressForOrganisationBuilder::init()
                            ->addressLine1('AddressLine14')
                            ->addressLine2('AddressLine20')
                            ->addressLine3('AddressLine38')
                            ->addressLine4('AddressLine46')
                            ->addressType(AddressType1Enum::DELIVERY)
                            ->build()
                    ]
                )
                ->baseCurrency(CurrencyCodeEnum::BND)
                ->class(Class1Enum::NON_GST_CASHBOOK)
                ->countryCode(CountryCodeEnum::PN)
                ->build(),
            OrganisationBuilder::init()
                ->aPIKey('APIKey4')
                ->addresses(
                    [
                        AddressForOrganisationBuilder::init()
                            ->addressLine1('AddressLine14')
                            ->addressLine2('AddressLine20')
                            ->addressLine3('AddressLine38')
                            ->addressLine4('AddressLine46')
                            ->addressType(AddressType1Enum::DELIVERY)
                            ->build(),
                        AddressForOrganisationBuilder::init()
                            ->addressLine1('AddressLine14')
                            ->addressLine2('AddressLine20')
                            ->addressLine3('AddressLine38')
                            ->addressLine4('AddressLine46')
                            ->addressType(AddressType1Enum::DELIVERY)
                            ->build(),
                        AddressForOrganisationBuilder::init()
                            ->addressLine1('AddressLine14')
                            ->addressLine2('AddressLine20')
                            ->addressLine3('AddressLine38')
                            ->addressLine4('AddressLine46')
                            ->addressType(AddressType1Enum::DELIVERY)
                            ->build()
                    ]
                )
                ->baseCurrency(CurrencyCodeEnum::BND)
                ->class(Class1Enum::NON_GST_CASHBOOK)
                ->countryCode(CountryCodeEnum::PN)
                ->build()
        ]
    )
    ->build();
```

