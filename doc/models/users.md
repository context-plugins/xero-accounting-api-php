
# Users

## Structure

`Users`

## Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `users` | [`?(User[])`](../../doc/models/user.md) | Optional | - | getUsers(): ?array | setUsers(?array users): void |

## Example

```php
use XeroAccountingAPILib\Models\Builders\UsersBuilder;
use XeroAccountingAPILib\Models\Builders\UserBuilder;
use XeroAccountingAPILib\Models\OrganisationRoleEnum;

$users = UsersBuilder::init()
    ->users(
        [
            UserBuilder::init()
                ->emailAddress('EmailAddress0')
                ->firstName('FirstName0')
                ->isSubscriber(false)
                ->lastName('LastName0')
                ->organisationRole(OrganisationRoleEnum::READONLY)
                ->build()
        ]
    )
    ->build();
```

