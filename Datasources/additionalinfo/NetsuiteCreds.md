<img  src="../../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../../images/RJOrbitLogo-2021Final.png" width="100">


# Credentials for NetSuite

[![Pre-Installation](../../images/Button_PreInstall.png)](guides/installguide.md)[![Installation](../../images/Button_Installation.png)](guides/installguide.md)[![Registration](../../images/Button_Registration.png)](guides/RegistrationGuide.md)[![Configuration](../../images/Button_Configuration.png)](guides/configurationGuide.md)[![Datasource](../../images/Button_Datasource.png)](Datasources/README.md)

---
{graphic for getting account id}

expand for account id


In NetSuite, log in as an administrator role and navigate to **Setup&rarr;Company&rarr;Enable Features&rarr;SuiteCloud&rarr;Manage Authentication**. 
Make sure Token-Based Authentication and TBA: Authorization Flow are checked and save changes.
![Manage Authentication](../../images/NetsuiteManageAuthentication.png)

Navigate to **Setup&rarr;Integration&rarr;Manage Integrations**. Create a new integration and select Token-Based Authentication. When the integration is created, the Consumer Key and Consumer Secret displayed will map directly to the OAuthClientId and OAuthClientSecret connection properties. Save these to a document.

![Manage Integrations](../../images/NetsuiteManageIntegrations.png)

Create a token role by navigating to **Setup&rarr;User/Roles&rarr;Manage Roles** and either create a new role or edit an existing role.
Under **Permissions&rarr;Setup**, the role must have the User Access Token: Full, Access Token Management: Full, and Web Services: Full permissions.
Add the role to a user under **Lists&rarr;Employees&rarr;Employees**. Select to edit an employee and add the new token role under **Access&rarr;Roles**.

![Manage Roles](../../images/NetsuiteManageRoles.png)

Navigate to **Setup&rarr;User/Roles&rarr;Access Tokens** and create a new access token. Select the application name as the integration that was created earlier, and the same user and role that were updated in the previous steps.
After creating the access token, a Token Id and Token Secret will be displayed. These map directly to the OAuthAccessToken and OAuthAccessTokenSecret. Save these to a document.

![AccessTokens](../../images/NetsuiteAccessTokens.png)

After creating the access token, a connection can now be made using the values obtained from the previous steps. Specify these connection properties at a minimum to connect:

**AccountId** specifying the account to connect to.
**OAuthClientId** the Consumer Key displayed when the application was created.
**OAuthClientSecret** the Consumer Secret displayed when the application was created.
**OAuthAccessToken** the Token Id when the access token was created.
**OAuthAccessTokenSecret** the Token Secret when the access token was created.