
# Quotes

## Structure

`Quotes`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `quotes` | [`?(Quote[])`](../../doc/models/quote.md) | Optional | - | getQuotes(): ?array | setQuotes(?array quotes): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\QuotesBuilder;
use XeroAccountingAPILib\Models\Builders\QuoteBuilder;
use XeroAccountingAPILib\Models\Builders\ContactBuilder;
use XeroAccountingAPILib\Models\Builders\AddressBuilder;
use XeroAccountingAPILib\Models\AddressTypeEnum;
use XeroAccountingAPILib\Models\Builders\AttachmentBuilder;
use XeroAccountingAPILib\Models\CurrencyCodeEnum;

$quotes = QuotesBuilder::init()
    ->quotes(
        [
            QuoteBuilder::init()
                ->brandingThemeID('00001082-0000-0000-0000-000000000000')
                ->contact(
                    ContactBuilder::init()
                        ->accountNumber('AccountNumber2')
                        ->accountsPayableTaxType('AccountsPayableTaxType2')
                        ->accountsReceivableTaxType('AccountsReceivableTaxType6')
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
                        ->build()
                )
                ->currencyCode(CurrencyCodeEnum::USD)
                ->currencyRate(75.08)
                ->date('Date4')
                ->build(),
            QuoteBuilder::init()
                ->brandingThemeID('00001082-0000-0000-0000-000000000000')
                ->contact(
                    ContactBuilder::init()
                        ->accountNumber('AccountNumber2')
                        ->accountsPayableTaxType('AccountsPayableTaxType2')
                        ->accountsReceivableTaxType('AccountsReceivableTaxType6')
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
                        ->build()
                )
                ->currencyCode(CurrencyCodeEnum::USD)
                ->currencyRate(75.08)
                ->date('Date4')
                ->build()
        ]
    )
    ->build();
```

