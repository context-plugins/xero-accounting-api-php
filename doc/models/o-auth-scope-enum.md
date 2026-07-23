
# O Auth Scope Enum

OAuth 2 scopes supported by the API

## Enumeration

`OAuthScopeEnum`

## Fields

| Name | Description |
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

## Example

```php
use XeroAccountingAPILib\Models\OAuthScopeEnum;

$oAuthScope = OAuthScopeEnum::ACCOUNTING_ATTACHMENTS;
```

