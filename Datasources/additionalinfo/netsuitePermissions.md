<img  src="../../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../../images/RJOrbitLogo-2021Final.png" width="100">


# Permission Configurations

[![Pre-Installation](../../images/Button_PreInstall.png)](../../README.md)[![Installation](../../images/Button_Installation.png)](guides/installguide.md)[![Registration](../../images/Button_Registration.png)](guides/RegistrationGuide.md)[![Configuration](../../images/Button_Configuration.png)](guides/configurationGuide.md)[![Datasource](../../images/Button_Datasource.png)](../README.md)

---

Permissions may be configured for a role in NetSuite under **Setup &rarr; Users/Roles &rarr; Mange Roles**. This page contains three lists of permissions, first the required permissions, then other permissions for fuller support and finally, permissions that may block log in or the download of data. Make sure you add all permissions from the required section, select any other permissions for the data replication you want and remove all permissions from the role that are listed in the Access Violations. 

Please be aware that it is not possible for us to provide an exhaustive list of permissions as NetSuite adds support for new entities and permissions with each version.

Please see this Oracle Document: [NetSuite Users & Roles](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_N284861.html) for more information on permissions.

## Required Permissions
Note: Most of the following permissions fall under the Permissions &rarr; Setup section for a role. All of the following permissions are required for RJWarehouse.

|Permission | Used For|
|---|---|
|Log in Using Access Tokens|	Allows the user to log in to REST / SOAP services with a token.|
|REST Web Services|	All REST requests including when Schema is set to SuiteQL, and support for RESTlets.|
|SOAP Web Services|	All SOAP requests including when Schema is set to SuiteTalk (default), test connection, and some requests for custom fields.|
|Custom <type> Fields (VIEW)|	Allows users to see custom fields of the given type. Used with IncludeCustomFieldColumns.|
|Custom Lists (VIEW)|	Allows displaying metadata for custom list tables. Used with IncludeCustomListTables.|
|Custom Record Types (VIEW)|	Allows displaying metadata for custom record tables. Used with IncludeCustomRecordTables.|
|Customer (VIEW)|	This specific permission is under Permissions &rarr; Lists. It is used for testing the connection in RESTlets.|
|Deleted Records (VIEW)|	Used for retrieving information on deleted records.|
|SuiteAnalytics Workbook (VIEW)|	Found under Permissions -> Reports. Required for SuiteQL access.|
|Other Custom Fields (VIEW)|	Allows users to see custom fields of the "other" type. Used with IncludeCustomFieldColumns.|
|User Access Token|	Allows a user to have tokens created for them via ether Token Based Authentication or Using OAuth Authentication.|

## Other Permissions

Note: Most of these permissions can be set for view-only to limit access if required.

|Section|Permission|Used For|
|---|---|---|
|Permissions &rarr; Custom Record|	[Custom Record Name]|	Access to the given custom record table|
|Permissions &rarr; Lists|	Accounts|	Access to the Account table	|
|Permissions &rarr; Lists|	Bins|	Access to the Bin table	|
|Permissions &rarr; Lists|	Calendar|	Access to the CalendarEvent table along with the Events permission|
|Permissions &rarr; Lists|	Cases|	Access to the SupportCase table	|
|Permissions &rarr; Lists|	Classes|	Access to the Classification table|
|Permissions &rarr; Lists|	Contacts|	Access to the Contact table	|
|Permissions &rarr; Lists|	Currency|	Access to the Currency table|
|Permissions &rarr; Lists|	Customers|	Access to the Customer table|
|Permissions &rarr; Lists|	Departments|	Access to the Department table|
|Permissions &rarr; Lists|	Documents and Files|	Access to the File and Folder tables|
|Permissions &rarr; Lists|	Employee Record|	Access to the Employee tables|
|Permissions &rarr; Lists|	Events|	Access to the CalendarEvent table along with the Calendars permission|
|Permissions &rarr; Lists|	Items|	Access to various Item tables such as DiscountItem, InventoryItem, NonInventoryItem, etc.|
|Permissions &rarr; Lists|	Locations|	Access to the Location table|
|Permissions &rarr; Lists|	Phone Calls|Access to the PhoneCall table|
|Permissions &rarr; Lists|	Project Tasks|	Access to the ProjectTask table|
|Permissions &rarr; Lists|	Subsidiaries|	Access to the Subsidiary table|
|Permissions &rarr; Lists|	Tasks|	Access to the Task table|
|Permissions &rarr; Lists|	Vendors|	Access to the Vendor table|
|Permissions &rarr; Transactions|	[Custom Transaction Name]|	Access to retrieving data from the specific custom transaction via the special Transactions table|
|Permissions &rarr; Transactions|	Build Assemblies|	Access to the AssemblyBuild table	|
|Permissions &rarr; Transactions|	CashSale|	Access to the CashSale table|
|Permissions &rarr; Transactions|	Cash Sale Refund|	Access to the CashRefund table|
|Permissions &rarr; Transactions|	Charge|	Access to the Charge table|
|Permissions &rarr; Transactions|	Check|	Access to the Check table|
|Permissions &rarr; Transactions|	Credit Memo|	Access to the CreditMemo table|
|Permissions &rarr; Transactions|	Customer Deposit|	Access to the Customer Deposit table	|
|Permissions &rarr; Transactions|	Customer Payment|	Access to the Customer Payment table	|
|Permissions &rarr; Transactions|  Customer Refund|	Access to the Customer Refund table	|
|Permissions &rarr; Transactions|	Deposit|	Access to the Deposit table	|
|Permissions &rarr; Transactions|	Fulfill Orders| Access to the ItemFulfillments table|
|Permissions &rarr; Transactions|	Invoice|	Access to the Invoice table|
|Permissions &rarr; Transactions|	Item Receipt|	Access to the ItemReceipt table	|
|Permissions &rarr; Transactions|	Intercompany Adjustments|	Access to Intercompany Journal Entries|
|Permissions &rarr; Transactions|	Opportunity|	Access to the Opportunity table|
|Permissions &rarr; Transactions|	Purchase Order|	Access to the PurchaseOrder table|
|Permissions &rarr; Transactions|	Sales Order|	Access to the SalesOrder table|
|Permissions &rarr; Transactions|	Transfer Order|	Access to the TransferOrder table|
|Permissions &rarr; Transactions|	Vendor| Return Authorization	Access to the VendorReturnAuthorization tableTransaction table|
|Permissions &rarr; Transactions|	Work Order|	Access to the WorkOrder table|
|Permissions &rarr; Transactions|	Access Payment Audit Log|	Access to the Payment Audit Log|
Permissions &rarr; Transactions|	Approve EFT|	Access to approvals of EFT|
|Permissions &rarr; Transactions|	Approve Online Bill Payments|	Access to approvals of Online Bill Payments|
|Permissions &rarr; Transactions|	Approve Vendor Payments|	Access to approvals of Vendor Payments|
|Permissions &rarr; Transactions|	Find Transaction|	Access to Transaction search options|
## Permission Access Violations

|Section|Permission|Note|
|---|---|---|
|Permissions &rarr; Setup|Access Token Management|While required during setup of the tokens, this can cause violations and prevent access to NetSuite once role is being used.|
|Permissions &rarr; Setup|	OAuth 2.0 Authorized Applications Management| Possible permission violation.|
|Permissions &rarr; Setup|Core Administration Permissions|This is a Two Factor Authorization trigger which can cause a permission violation. However 2FA is being deprecated by NetSuite. Current ETA is unknown but removing this permission is best practice.|
|Permissions &rarr; Setup|	Two-Factor Authentication base| 2FA Trigger, see above.|
|Permissions &rarr; Setup|Set Up OpenID Connect (OIDC) Single Sign-on|	 Possible permission violation.|
|Permissions &rarr; Setup|Set Up OpenID Single Sign-on|	 Possible permission violation.|
|Permissions &rarr; Setup|Set Up SAML Single Sign-on|	 Possible permission violation.|
|Permissions &rarr; Setup|Integration Application|2FA Trigger, see above.|
|Permissions &rarr; Setup|Device ID Management|	2FA Trigger, see above.|
|Permissions &rarr; Setup|View Unencrypted Credit Cards|2FA Trigger, see above.|
[Previous](../netsuite.md)