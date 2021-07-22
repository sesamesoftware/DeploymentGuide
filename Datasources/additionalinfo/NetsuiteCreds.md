<a href="http://www.sesamesoftware.com"><img align=left src="../../images/RJOrbit110x110.png"></img></a>

# Credentials for NetSuite

[[Installation](../installguide.md)] [[Registration](../RegistrationGuide.md)] [[Configuration](../configurationGuide.md)] [[Datasource](../DatasourceGuide.md)]

---
## Required Information for NetSuite Connection

* **Account ID**
* **Role ID**
* **Authorization Tokens**


1. In NetSuite, log in as an administrator role and navigate to **Setup&rarr;Company&rarr;Company Information**. Save the Account ID to a .txt or other easy-to-find document.

![account id](../../images/NetsuiteAccountId.png)

2. Navigate to **Setup&rarr;Company&rarr;Enable Features&rarr;SuiteCloud&rarr;Manage Authentication**.
3. Make sure Token-Based Authentication and TBA: Authorization Flow are checked and save changes.
![Manage Authentication](../../images/NetsuiteManageAuthentication.png)

4. Navigate to **Setup&rarr;Integration&rarr;Manage Integrations**.
5. Create a new integration and select Token-Based Authentication. When the integration is created, the Consumer Key and Consumer Secret displayed will map directly to the OAuthClientId and OAuthClientSecret connection properties in RJWarehouse. Save the Application ID and the keys to the document where you saved the Account ID.

![Manage Integrations](../../images/NetsuiteManageIntegrations.png)

6. Create a token role by navigating to **Setup&rarr;User/Roles&rarr;Manage Roles** and either create a new role for RJWarehouse to use or edit an existing role with the required configuration and permissions
   1. See [Role Creation, Modification and Setting Permissions](../../images/netsuitepermissions.md) for more information on the requirements for roles and permissions.

7. Add the role to a user under **Lists&rarr;Employees&rarr;Employees**. Select to edit an employee and add the new token role under **Access&rarr;Roles**.

![Manage Roles](../../images/NetsuiteManageRoles.png)

9. Navigate to **Setup&rarr;User/Roles&rarr;Access Tokens** and create a new access token. Select the application name as the integration that was created earlier, and the same user and role that were updated in the previous steps.
10. After creating the access token, a Token Id and Token Secret will be displayed. These map directly to the OAuthAccessToken and OAuthAccessTokenSecret. Save these to the document.

![AccessTokens](../../images/NetsuiteAccessTokens.png)

You should not have the following information:

**AccountId** specifying the account to connect to.
**OAuthClientId** the Consumer Key displayed when the application was created.
**OAuthClientSecret** the Consumer Secret displayed when the application was created.
**OAuthAccessToken** the Token Id when the access token was created.
**OAuthAccessTokenSecret** the Token Secret when the access token was created.

---

[[&#9664; Back to NetSuite Datasource](../netsuite.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../../images/poweredBy.png" height="80px"></img></a> </p>
