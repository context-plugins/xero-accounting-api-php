
# Contact

Find out more here: [http://developer.xero.com/documentation/api/contacts/](http://developer.xero.com/documentation/api/contacts/)

## Structure

`Contact`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `accountNumber` | `?string` | Optional | A user defined account number. This can be updated via the API and the Xero UI (max length = 50)<br><br>**Constraints**: *Maximum Length*: `50` | getAccountNumber(): ?string | setAccountNumber(?string accountNumber): void |
| `accountsPayableTaxType` | `?string` | Optional | The tax type from TaxRates | getAccountsPayableTaxType(): ?string | setAccountsPayableTaxType(?string accountsPayableTaxType): void |
| `accountsReceivableTaxType` | `?string` | Optional | The tax type from TaxRates | getAccountsReceivableTaxType(): ?string | setAccountsReceivableTaxType(?string accountsReceivableTaxType): void |
| `addresses` | [`?(Address[])`](../../doc/models/address.md) | Optional | Store certain address types for a contact – see address types | getAddresses(): ?array | setAddresses(?array addresses): void |
| `attachments` | [`?(Attachment[])`](../../doc/models/attachment.md) | Optional | Displays array of attachments from the API | getAttachments(): ?array | setAttachments(?array attachments): void |
| `balances` | [`?Balances`](../../doc/models/balances.md) | Optional | The raw AccountsReceivable(sales invoices) and AccountsPayable(bills) outstanding and overdue amounts, not converted to base currency (read only) | getBalances(): ?Balances | setBalances(?Balances balances): void |
| `bankAccountDetails` | `?string` | Optional | Bank account number of contact | getBankAccountDetails(): ?string | setBankAccountDetails(?string bankAccountDetails): void |
| `batchPayments` | [`?BatchPaymentDetails`](../../doc/models/batch-payment-details.md) | Optional | Bank details for use on a batch payment stored with each contact<br><br>Find out more here: [http://developer.xero.com/documentation/api/Contact/](http://developer.xero.com/documentation/api/Contact/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/Contact/](http://developer.xero.com/documentation/api/Contact/) | getBatchPayments(): ?BatchPaymentDetails | setBatchPayments(?BatchPaymentDetails batchPayments): void |
| `brandingTheme` | [`?BrandingTheme`](../../doc/models/branding-theme.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/branding-themes/](http://developer.xero.com/documentation/api/branding-themes/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/branding-themes/](http://developer.xero.com/documentation/api/branding-themes/) | getBrandingTheme(): ?BrandingTheme | setBrandingTheme(?BrandingTheme brandingTheme): void |
| `contactGroups` | [`?(ContactGroup[])`](../../doc/models/contact-group.md) | Optional | Displays which contact groups a contact is included in | getContactGroups(): ?array | setContactGroups(?array contactGroups): void |
| `contactID` | `?string` | Optional | Xero identifier | getContactID(): ?string | setContactID(?string contactID): void |
| `contactNumber` | `?string` | Optional | This can be updated via the API only i.e. This field is read only on the Xero contact screen, used to identify contacts in external systems (max length = 50). If the Contact Number is used, this is displayed as Contact Code in the Contacts UI in Xero.<br><br>**Constraints**: *Maximum Length*: `50` | getContactNumber(): ?string | setContactNumber(?string contactNumber): void |
| `contactPersons` | [`?(ContactPerson[])`](../../doc/models/contact-person.md) | Optional | See contact persons | getContactPersons(): ?array | setContactPersons(?array contactPersons): void |
| `contactStatus` | [`?string(ContactStatusEnum)`](../../doc/models/contact-status-enum.md) | Optional | Current status of a contact – see contact status types | getContactStatus(): ?string | setContactStatus(?string contactStatus): void |
| `defaultCurrency` | [`?string(CurrencyCodeEnum)`](../../doc/models/currency-code-enum.md) | Optional | 3 letter alpha code for the currency – see list of currency codes | getDefaultCurrency(): ?string | setDefaultCurrency(?string defaultCurrency): void |
| `discount` | `?float` | Optional, Read-only | The default discount rate for the contact (read only) | getDiscount(): ?float | setDiscount(?float discount): void |
| `emailAddress` | `?string` | Optional | Email address of contact person (umlauts not supported) (max length  = 255)<br><br>**Constraints**: *Maximum Length*: `255` | getEmailAddress(): ?string | setEmailAddress(?string emailAddress): void |
| `firstName` | `?string` | Optional | First name of contact person (max length = 255)<br><br>**Constraints**: *Maximum Length*: `255` | getFirstName(): ?string | setFirstName(?string firstName): void |
| `hasAttachments` | `?bool` | Optional | A boolean to indicate if a contact has an attachment<br><br>**Default**: `false` | getHasAttachments(): ?bool | setHasAttachments(?bool hasAttachments): void |
| `hasValidationErrors` | `?bool` | Optional | A boolean to indicate if a contact has an validation errors<br><br>**Default**: `false` | getHasValidationErrors(): ?bool | setHasValidationErrors(?bool hasValidationErrors): void |
| `isCustomer` | `?bool` | Optional | true or false – Boolean that describes if a contact has any AR invoices entered against them. Cannot be set via PUT or POST – it is automatically set when an accounts receivable invoice is generated against this contact. | getIsCustomer(): ?bool | setIsCustomer(?bool isCustomer): void |
| `isSupplier` | `?bool` | Optional | true or false – Boolean that describes if a contact that has any AP  invoices entered against them. Cannot be set via PUT or POST – it is automatically set when an accounts payable invoice is generated against this contact. | getIsSupplier(): ?bool | setIsSupplier(?bool isSupplier): void |
| `lastName` | `?string` | Optional | Last name of contact person (max length = 255)<br><br>**Constraints**: *Maximum Length*: `255` | getLastName(): ?string | setLastName(?string lastName): void |
| `name` | `?string` | Optional | Full name of contact/organisation (max length = 255)<br><br>**Constraints**: *Maximum Length*: `255` | getName(): ?string | setName(?string name): void |
| `paymentTerms` | [`?PaymentTerm`](../../doc/models/payment-term.md) | Optional | Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/)<br><br>Find out more here: [http://developer.xero.com/documentation/api/organisation/](http://developer.xero.com/documentation/api/organisation/) | getPaymentTerms(): ?PaymentTerm | setPaymentTerms(?PaymentTerm paymentTerms): void |
| `phones` | [`?(Phone[])`](../../doc/models/phone.md) | Optional | Store certain phone types for a contact – see phone types | getPhones(): ?array | setPhones(?array phones): void |
| `purchasesDefaultAccountCode` | `?string` | Optional | The default purchases account code for contacts | getPurchasesDefaultAccountCode(): ?string | setPurchasesDefaultAccountCode(?string purchasesDefaultAccountCode): void |
| `purchasesTrackingCategories` | [`?(SalesTrackingCategory[])`](../../doc/models/sales-tracking-category.md) | Optional | The default purchases tracking categories for contacts | getPurchasesTrackingCategories(): ?array | setPurchasesTrackingCategories(?array purchasesTrackingCategories): void |
| `salesDefaultAccountCode` | `?string` | Optional | The default sales account code for contacts | getSalesDefaultAccountCode(): ?string | setSalesDefaultAccountCode(?string salesDefaultAccountCode): void |
| `salesTrackingCategories` | [`?(SalesTrackingCategory[])`](../../doc/models/sales-tracking-category.md) | Optional | The default sales tracking categories for contacts | getSalesTrackingCategories(): ?array | setSalesTrackingCategories(?array salesTrackingCategories): void |
| `skypeUserName` | `?string` | Optional | Skype user name of contact | getSkypeUserName(): ?string | setSkypeUserName(?string skypeUserName): void |
| `statusAttributeString` | `?string` | Optional | Status of object | getStatusAttributeString(): ?string | setStatusAttributeString(?string statusAttributeString): void |
| `taxNumber` | `?string` | Optional | Tax number of contact – this is also known as the ABN (Australia), GST Number (New Zealand), VAT Number (UK) or Tax ID Number (US and global) in the Xero UI depending on which regionalized version of Xero you are using (max length = 50)<br><br>**Constraints**: *Maximum Length*: `50` | getTaxNumber(): ?string | setTaxNumber(?string taxNumber): void |
| `trackingCategoryName` | `?string` | Optional | The name of the Tracking Category assigned to the contact under SalesTrackingCategories and PurchasesTrackingCategories | getTrackingCategoryName(): ?string | setTrackingCategoryName(?string trackingCategoryName): void |
| `trackingCategoryOption` | `?string` | Optional | The name of the Tracking Option assigned to the contact under SalesTrackingCategories and PurchasesTrackingCategories | getTrackingCategoryOption(): ?string | setTrackingCategoryOption(?string trackingCategoryOption): void |
| `updatedDateUTC` | `?string` | Optional, Read-only | UTC timestamp of last update to contact | getUpdatedDateUTC(): ?string | setUpdatedDateUTC(?string updatedDateUTC): void |
| `validationErrors` | [`?(ValidationError[])`](../../doc/models/validation-error.md) | Optional | Displays validation errors returned from the API | getValidationErrors(): ?array | setValidationErrors(?array validationErrors): void |
| `website` | `?string` | Optional, Read-only | Website address for contact (read only) | getWebsite(): ?string | setWebsite(?string website): void |
| `xeroNetworkKey` | `?string` | Optional | Store XeroNetworkKey for contacts. | getXeroNetworkKey(): ?string | setXeroNetworkKey(?string xeroNetworkKey): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;

$contact = ContactBuilder::init()
    ->accountNumber('AccountNumber6')
    ->accountsPayableTaxType('AccountsPayableTaxType6')
    ->accountsReceivableTaxType('AccountsReceivableTaxType2')
    ->addresses(
        [
            AddressBuilder::init()
                ->addressLine1('AddressLine14')
                ->addressLine2('AddressLine20')
                ->addressLine3('AddressLine38')
                ->addressLine4('AddressLine46')
                ->addressType(AddressTypeEnum::POBOX)
                ->build()
        ]
    )
    ->attachments(
        [
            AttachmentBuilder::init()
                ->attachmentID('00000714-0000-0000-0000-000000000000')
                ->contentLength(34)
                ->fileName('FileName6')
                ->includeOnline(false)
                ->mimeType('MimeType6')
                ->build(),
            AttachmentBuilder::init()
                ->attachmentID('00000714-0000-0000-0000-000000000000')
                ->contentLength(34)
                ->fileName('FileName6')
                ->includeOnline(false)
                ->mimeType('MimeType6')
                ->build()
        ]
    )
    ->hasAttachments(false)
    ->hasValidationErrors(false)
    ->updatedDateUTC('/Date(1573755038314)/')
    ->build();
```

