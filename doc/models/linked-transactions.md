
# Linked Transactions

## Structure

`LinkedTransactions`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `linkedTransactions` | [`?(LinkedTransaction[])`](../../doc/models/linked-transaction.md) | Optional | - | getLinkedTransactions(): ?array | setLinkedTransactions(?array linkedTransactions): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\LinkedTransactionsBuilder;
use XeroAccountingAPILib\Models\Builders\LinkedTransactionBuilder;
use XeroAccountingAPILib\Models\SourceTransactionTypeCodeEnum;

$linkedTransactions = LinkedTransactionsBuilder::init()
    ->linkedTransactions(
        [
            LinkedTransactionBuilder::init()
                ->contactID('00001a8c-0000-0000-0000-000000000000')
                ->linkedTransactionID('00000836-0000-0000-0000-000000000000')
                ->sourceLineItemID('0000017e-0000-0000-0000-000000000000')
                ->sourceTransactionID('00001c84-0000-0000-0000-000000000000')
                ->sourceTransactionTypeCode(SourceTransactionTypeCodeEnum::ACCPAY)
                ->build()
        ]
    )
    ->build();
```

