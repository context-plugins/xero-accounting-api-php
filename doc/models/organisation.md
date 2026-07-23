
# Organisation

Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/)

## Structure

`Organisation`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `aPIKey` | `?string` | Optional | Display a unique key used for Xero-to-Xero transactions | getAPIKey(): ?string | setAPIKey(?string aPIKey): void |
| `addresses` | [`?(AddressForOrganisation[])`](../../doc/models/address-for-organisation.md) | Optional | Address details for organisation – see Addresses | getAddresses(): ?array | setAddresses(?array addresses): void |
| `baseCurrency` | [`?string(CurrencyCodeEnum)`](../../doc/models/currency-code-enum.md) | Optional | 3 letter alpha code for the currency – see list of currency codes | getBaseCurrency(): ?string | setBaseCurrency(?string baseCurrency): void |
| `class` | [`?string(Class1Enum)`](../../doc/models/class-1-enum.md) | Optional | Organisation Classes describe which plan the Xero organisation is on (e.g. DEMO, TRIAL, PREMIUM) | getClass(): ?string | setClass(?string class): void |
| `countryCode` | [`?string(CountryCodeEnum)`](../../doc/models/country-code-enum.md) | Optional | - | getCountryCode(): ?string | setCountryCode(?string countryCode): void |
| `createdDateUTC` | `?string` | Optional, Read-only | Timestamp when the organisation was created in Xero | getCreatedDateUTC(): ?string | setCreatedDateUTC(?string createdDateUTC): void |
| `defaultPurchasesTax` | `?string` | Optional | The default for LineAmountTypes on purchase transactions | getDefaultPurchasesTax(): ?string | setDefaultPurchasesTax(?string defaultPurchasesTax): void |
| `defaultSalesTax` | `?string` | Optional | The default for LineAmountTypes on sales transactions | getDefaultSalesTax(): ?string | setDefaultSalesTax(?string defaultSalesTax): void |
| `edition` | [`?string(EditionEnum)`](../../doc/models/edition-enum.md) | Optional | BUSINESS or PARTNER. Partner edition organisations are sold exclusively through accounting partners and have restricted functionality (e.g. no access to invoicing) | getEdition(): ?string | setEdition(?string edition): void |
| `employerIdentificationNumber` | `?string` | Optional | Shown if set. US Only. | getEmployerIdentificationNumber(): ?string | setEmployerIdentificationNumber(?string employerIdentificationNumber): void |
| `endOfYearLockDate` | `?string` | Optional | Shown if set. See lock dates | getEndOfYearLockDate(): ?string | setEndOfYearLockDate(?string endOfYearLockDate): void |
| `externalLinks` | [`?(ExternalLink[])`](../../doc/models/external-link.md) | Optional | Organisation profile links for popular services such as Facebook,Twitter, GooglePlus and LinkedIn. You can also add link to your website here. Shown if Organisation settings  is updated in Xero. See ExternalLinks below | getExternalLinks(): ?array | setExternalLinks(?array externalLinks): void |
| `financialYearEndDay` | `?int` | Optional | Calendar day e.g. 0-31 | getFinancialYearEndDay(): ?int | setFinancialYearEndDay(?int financialYearEndDay): void |
| `financialYearEndMonth` | `?int` | Optional | Calendar Month e.g. 1-12 | getFinancialYearEndMonth(): ?int | setFinancialYearEndMonth(?int financialYearEndMonth): void |
| `isDemoCompany` | `?bool` | Optional | Boolean to describe if organisation is a demo company. | getIsDemoCompany(): ?bool | setIsDemoCompany(?bool isDemoCompany): void |
| `legalName` | `?string` | Optional | Organisation name shown on Reports | getLegalName(): ?string | setLegalName(?string legalName): void |
| `lineOfBusiness` | `?string` | Optional | Description of business type as defined in Organisation settings | getLineOfBusiness(): ?string | setLineOfBusiness(?string lineOfBusiness): void |
| `name` | `?string` | Optional | Display name of organisation shown in Xero | getName(): ?string | setName(?string name): void |
| `organisationEntityType` | [`?string(OrganisationEntityTypeEnum)`](../../doc/models/organisation-entity-type-enum.md) | Optional | Organisation Entity Type | getOrganisationEntityType(): ?string | setOrganisationEntityType(?string organisationEntityType): void |
| `organisationID` | `?string` | Optional | Unique Xero identifier | getOrganisationID(): ?string | setOrganisationID(?string organisationID): void |
| `organisationStatus` | `?string` | Optional | Will be set to ACTIVE if you can connect to organisation via the Xero API | getOrganisationStatus(): ?string | setOrganisationStatus(?string organisationStatus): void |
| `organisationType` | [`?string(OrganisationTypeEnum)`](../../doc/models/organisation-type-enum.md) | Optional | Organisation Type | getOrganisationType(): ?string | setOrganisationType(?string organisationType): void |
| `paymentTerms` | [`?PaymentTerm`](../../doc/models/payment-term.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/) | getPaymentTerms(): ?PaymentTerm | setPaymentTerms(?PaymentTerm paymentTerms): void |
| `paysTax` | `?bool` | Optional | Boolean to describe if organisation is registered with a local tax authority i.e. true, false | getPaysTax(): ?bool | setPaysTax(?bool paysTax): void |
| `periodLockDate` | `?string` | Optional | Shown if set. See lock dates | getPeriodLockDate(): ?string | setPeriodLockDate(?string periodLockDate): void |
| `phones` | [`?(Phone[])`](../../doc/models/phone.md) | Optional | Phones details for organisation – see Phones | getPhones(): ?array | setPhones(?array phones): void |
| `registrationNumber` | `?string` | Optional | Shows for New Zealand, Australian and UK organisations | getRegistrationNumber(): ?string | setRegistrationNumber(?string registrationNumber): void |
| `salesTaxBasis` | [`?string(SalesTaxBasisEnum)`](../../doc/models/sales-tax-basis-enum.md) | Optional | The accounting basis used for tax returns. See Sales Tax Basis | getSalesTaxBasis(): ?string | setSalesTaxBasis(?string salesTaxBasis): void |
| `salesTaxPeriod` | [`?string(SalesTaxPeriodEnum)`](../../doc/models/sales-tax-period-enum.md) | Optional | The frequency with which tax returns are processed. See Sales Tax Period | getSalesTaxPeriod(): ?string | setSalesTaxPeriod(?string salesTaxPeriod): void |
| `shortCode` | `?string` | Optional | A unique identifier for the organisation. Potential uses. | getShortCode(): ?string | setShortCode(?string shortCode): void |
| `taxNumber` | `?string` | Optional | Shown if set. Displays in the Xero UI as Tax File Number (AU), GST Number (NZ), VAT Number (UK) and Tax ID Number (US & Global). | getTaxNumber(): ?string | setTaxNumber(?string taxNumber): void |
| `timezone` | [`?string(TimeZoneEnum)`](../../doc/models/time-zone-enum.md) | Optional | Timezone specifications | getTimezone(): ?string | setTimezone(?string timezone): void |
| `version` | [`?string(VersionEnum)`](../../doc/models/version-enum.md) | Optional | See Version Types | getVersion(): ?string | setVersion(?string version): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\OrganisationBuilder;
use XeroAccountingAPILib\Models\Builders\AddressForOrganisationBuilder;
use XeroAccountingAPILib\Models\AddressType1Enum;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;
use XeroAccountingAPILib\Models\Class1Enum;
use XeroAccountingAPILib\Models\CountryCodeEnum;

$organisation = OrganisationBuilder::init()
    ->aPIKey('APIKey6')
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
                ->build()
        ]
    )
    ->baseCurrency(CurrencyCodeEnum::CAD)
    ->class(Class1Enum::DEMO)
    ->countryCode(CountryCodeEnum::MS)
    ->createdDateUTC('/Date(1573755038314)/')
    ->organisationID('8be9db36-3598-4755-ba5c-c2dbc8c4a7a2')
    ->build();
```

