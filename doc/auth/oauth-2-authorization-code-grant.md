
# OAuth 2 Authorization Code Grant



Documentation for accessing and setting credentials for OAuth2.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| OAuthClientId | `string` | OAuth 2 Client ID | `oAuthClientId` | `getOAuthClientId()` |
| OAuthClientSecret | `string` | OAuth 2 Client Secret | `oAuthClientSecret` | `getOAuthClientSecret()` |
| OAuthRedirectUri | `string` | OAuth 2 Redirection endpoint or Callback Uri | `oAuthRedirectUri` | `getOAuthRedirectUri()` |
| OAuthToken | `OAuthToken\|null` | Object for storing information about the OAuth token | `oAuthToken` | `getOAuthToken()` |
| OAuthScopes | `string[]\|null` | List of scopes that apply to the OAuth token | `oAuthScopes` | `getOAuthScopes()` |
| OAuthClockSkew | `int` | Clock skew time in seconds applied while checking the OAuth Token expiry. | `oAuthClockSkew` | - |



**Note:** Auth credentials can be set using `AuthorizationCodeAuthCredentialsBuilder::init()` in `authorizationCodeAuthCredentials` method in the client builder and accessed through `getAuthorizationCodeAuth` method in the client instance.

## Usage Example

### 1\. Client Initialization

You must initialize the client with *OAuth 2.0 Authorization Code Grant* credentials as shown in the following code snippet.

```php
use XeroAccountingAPILib\Authentication\AuthorizationCodeAuthCredentialsBuilder;
use XeroAccountingAPILib\Models\OAuthScopeEnum;
use XeroAccountingAPILib\XeroAccountingAPIClientBuilder;

$client = XeroAccountingAPIClientBuilder::init()
    ->authorizationCodeAuthCredentials(
        AuthorizationCodeAuthCredentialsBuilder::init(
            'OAuthClientId',
            'OAuthClientSecret',
            'OAuthRedirectUri'
        )
            ->oAuthScopes(
                [
                    OAuthScopeEnum::ACCOUNTING_ATTACHMENTS,
                    OAuthScopeEnum::ACCOUNTING_ATTACHMENTS_READ
                ]
            )
    )
    ->build();
```



Your application must obtain user authorization before it can execute an endpoint call in case this SDK chooses to use *OAuth 2.0 Authorization Code Grant*. This authorization includes the following steps

### 2\. Obtain user consent

To obtain user's consent, you must redirect the user to the authorization page.The `buildAuthorizationUrl()` method creates the URL to the authorization page. You must have initialized the client with scopes for which you need permission to access.

```php
$authUrl = $client->getAuthorizationCodeAuth()->buildAuthorizationUrl();
header('Location: ' . filter_var($authUrl, FILTER_SANITIZE_URL));
```

### 3\. Handle the OAuth server response

Once the user responds to the consent request, the OAuth 2.0 server responds to your application's access request by redirecting the user to the redirect URI specified set in `Configuration`.

If the user approves the request, the authorization code will be sent as the `code` query string:

```
https://example.com/oauth/callback?code=XXXXXXXXXXXXXXXXXXXXXXXXX
```

If the user does not approve the request, the response contains an `error` query string:

```
https://example.com/oauth/callback?error=access_denied
```

### 4\. Authorize the client using the code

After the server receives the code, it can exchange this for an *access token*. The access token is an object containing information for authorizing client requests and refreshing the token itself.

```php
try {
    $token = $client->getAuthorizationCodeAuth()->fetchToken($_GET['code']);
    // re-build the client with oauth token
    $client = $client
        ->toBuilder()
        ->authorizationCodeAuthCredentials(
            $client->getAuthorizationCodeAuthCredentialsBuilder()->oAuthToken($token)
        )
        ->build();
} catch (XeroAccountingAPILib\Exceptions\ApiException $e) {
    // handle exception
}
```

### Scopes

Scopes enable your application to only request access to the resources it needs while enabling users to control the amount of access they grant to your application. Available scopes are defined in the [`OAuthScopeEnum`](../../doc/models/o-auth-scope-enum.md) enumeration.

| Scope Name | Description |
|  --- | --- |
| `ACCOUNTING_ATTACHMENTS` | Grant read-write access to attachments |
| `ACCOUNTING_ATTACHMENTS_READ` | Grant read-only access to attachments |
| `ACCOUNTING_CONTACTS` | Grant read-write access to contacts and contact groups |
| `ACCOUNTING_CONTACTS_READ` | Grant read-only access to contacts and contact groups |
| `ACCOUNTING_JOURNALS_READ` | Grant read-only access to journals |
| `ACCOUNTING_REPORTS_READ` | Grant read-only access to accounting reports |
| `ACCOUNTING_REPORTS_TENNINETYNINE_READ` | Grant read-only access to 1099 reports |
| `ACCOUNTING_SETTINGS` | Grant read-write access to organisation and account settings |
| `ACCOUNTING_SETTINGS_READ` | Grant read-only access to organisation and account settings |
| `ACCOUNTING_TRANSACTIONS` | Grant read-write access to bank transactions, credit notes, invoices, repeating invoices |
| `ACCOUNTING_TRANSACTIONS_READ` | Grant read-only access to invoices |
| `ASSETS` | Grant read-write access to assets |
| `ASSETS_READ` | Grant read-only access to fixed assets |
| `BANKFEEDS` | Grant read-write access to bankfeeds |
| `EMAIL` | Grant read-only access to your email |
| `FILES` | Grant read-write access to files and folders |
| `FILES_READ` | Grant read-only access to files and folders |
| `OPENID` | Grant read-only access to your open id |
| `PAYMENTSERVICES` | Grant read-write access to payment services |
| `PAYROLL` | Grant read-write access to payroll |
| `PAYROLL_EMPLOYEES` | Grant read-write access to payroll employees |
| `PAYROLL_EMPLOYEES_READ` | Grant read-only access to payroll employees |
| `PAYROLL_LEAVEAPPLICATIONS` | Grant read-write access to payroll leaveapplications |
| `PAYROLL_LEAVEAPPLICATIONS_READ` | Grant read-only access to payroll leaveapplications |
| `PAYROLL_PAYITEMS` | Grant read-write access to payroll payitems |
| `PAYROLL_PAYITEMS_READ` | Grant read-only access to payroll payitems |
| `PAYROLL_PAYROLLCALENDARS` | Grant read-write access to payroll calendars |
| `PAYROLL_PAYROLLCALENDARS_READ` | Grant read-only access to payroll calendars |
| `PAYROLL_PAYRUNS` | Grant read-write access to payroll payruns |
| `PAYROLL_PAYRUNS_READ` | Grant read-only access to payroll payruns |
| `PAYROLL_PAYSLIP` | Grant read-write access to payroll payslips |
| `PAYROLL_PAYSLIP_READ` | Grant read-only access to payroll payslips |
| `PAYROLL_READ` | Grant read-only access to payroll |
| `PAYROLL_SETTINGS_READ` | Grant read-only access to payroll settings |
| `PAYROLL_SUPERFUNDPRODUCTS_READ` | Grant read-only access to payroll superfundproducts |
| `PAYROLL_SUPERFUNDS` | Grant read-write access to payroll superfunds |
| `PAYROLL_SUPERFUNDS_READ` | Grant read-only access to payroll superfunds |
| `PAYROLL_TIMESHEETS` | Grant read-write access to payroll timesheets |
| `PAYROLL_TIMESHEETS_READ` | Grant read-only access to payroll timesheets |
| `PROFILE` | your profile information |
| `PROJECTS` | Grant read-write access to projects |
| `PROJECTS_READ` | Grant read-only access to projects |

### Refreshing the token

An access token may expire after sometime. To extend its lifetime, you must refresh the token.

```php
if ($client->getAuthorizationCodeAuth()->isTokenExpired()) {
    try {
        $token = $client->getAuthorizationCodeAuth()->refreshToken();
        // re-build the client with oauth token
        $client = $client
            ->toBuilder()
            ->authorizationCodeAuthCredentials(
                $client->getAuthorizationCodeAuthCredentialsBuilder()->oAuthToken($token)
            )
            ->build();
    } catch (XeroAccountingAPILib\Exceptions\ApiException $e) {
        // handle exception
    }
}
```

If a token expires, an exception will be thrown before the next endpoint call requiring authentication.

### Storing an access token for reuse

It is recommended that you store the access token for reuse.

```php
// store token
$_SESSION['access_token'] = $client->getAuthorizationCodeAuth()->getOAuthToken();
```

### Creating a client from a stored token

To authorize a client using a stored access token, just set the access token in Configuration along with the other configuration parameters before creating the client:

```php
// load token later...
$token = $_SESSION['access_token'];

// re-build the client with oauth token
$client = $client
    ->toBuilder()
    ->authorizationCodeAuthCredentials($client->getAuthorizationCodeAuthCredentialsBuilder()->oAuthToken($token))
    ->build();
```

### Complete example



```php
<?php
require_once __DIR__.'/vendor/autoload.php';

session_start();

use XeroAccountingAPILib\Environment;
use XeroAccountingAPILib\Authentication\AuthorizationCodeAuthCredentialsBuilder;
use XeroAccountingAPILib\Models\OAuthScopeEnum;
use XeroAccountingAPILib\XeroAccountingAPIClientBuilder;

$client = XeroAccountingAPIClientBuilder::init()
    ->authorizationCodeAuthCredentials(
        AuthorizationCodeAuthCredentialsBuilder::init(
            'OAuthClientId',
            'OAuthClientSecret',
            'OAuthRedirectUri'
        )
            ->oAuthScopes(
                [
                    OAuthScopeEnum::ACCOUNTING_ATTACHMENTS,
                    OAuthScopeEnum::ACCOUNTING_ATTACHMENTS_READ
                ]
            )
    )
    ->environment(Environment::PRODUCTION)
    ->build();


// Obtain access token, restore from cache if possible
if (isset($_SESSION['access_token'])) {
    $token = $_SESSION['access_token'];
    // re-build the client with oauth token
    $client = $client
        ->toBuilder()
        ->authorizationCodeAuthCredentials(
            $client->getAuthorizationCodeAuthCredentialsBuilder()->oAuthToken($token)
        )
        ->build();
} else {
    try {
        // build authorization url to redirect the user
        $oAuthRedirectUri = $client->getAuthorizationCodeAuth()->buildAuthorizationUrl();
        // redirect the user to $oAuthRedirectUri and get a code after the user consent
        header('Location: ' . filter_var($oAuthRedirectUri, FILTER_SANITIZE_URL));

        // fetch an oauth token to authorize the client using the stored code
        $token = $client->getAuthorizationCodeAuth()->fetchToken($_GET['code']);
        // re-build the client with oauth token
        $client = $client
            ->toBuilder()
            ->authorizationCodeAuthCredentials(
                $client->getAuthorizationCodeAuthCredentialsBuilder()->oAuthToken($token)
            )
            ->build();

        // store token
        $_SESSION['access_token'] = $token;
    } catch (XeroAccountingAPILib\Exceptions\ApiException $e) {
        // handle exception
    }
}

// check if token gets expired, then try to refresh the token
if ($client->getAuthorizationCodeAuth()->isTokenExpired()) {
    try {
        // refresh the token
        $token = $client->getAuthorizationCodeAuth()->refreshToken();
        // re-build the client with oauth token
        $client = $client
            ->toBuilder()
            ->authorizationCodeAuthCredentials(
                $client->getAuthorizationCodeAuthCredentialsBuilder()->oAuthToken($token)
            )
            ->build();

        // update the cached token
        $_SESSION['access_token'] = $token;
    } catch (XeroAccountingAPILib\Exceptions\ApiException $e) {
        // handle exception
    }
}

// the client is now authorized; you can use $client to make endpoint calls
```


