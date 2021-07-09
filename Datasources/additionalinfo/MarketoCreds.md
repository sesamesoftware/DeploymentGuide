<img  src="../../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../../images/RJOrbitLogo-2021Final.png" width="100">

# Credentials for Marketo

[![Installation](../../images/Button_Installation.png)](../../guides/installguide.md)[![Registration](../../images/Button_Registration.png)](../../guides/RegistrationGuide.md)[![Configuration](../../images/Button_Configuration.png)](../../guides/configurationGuide.md)[![Datasource](../../images/Button_Datasource.png)](../README.md)

---

## Grant Permissions

1. Navigate to **Admin&rarr;Security&rarr;Users & Roles**
2. Create a new role and grant permissions to the required APIs.
![account id](../../images/MarketoCreds1.PNG)

## Obtaining an API Token

1. Navigate to **Admin&rarr;Integration&rarr;Launch Point**
![Manage Authentication](../../images/MarketoCreds2.PNG)
2. Click **View Details** and the following form displays
![Manage Authentication](../../images/MarketoCreds3.PNG)
3. If you click **Get Token**, a new token will be generated.
Input the token into **OAuthAccessToken** property in the Open Authorization Information tab
After creating the access token, a connection can now be made using the values obtained from the previous steps. Specify these connection properties at a minimum to connect:

- **OAuthAccessToken** the Token Id when the access token was created.
- **OAuthClientId** the Consumer Key displayed when the application was created.
- **OAuthClientSecret** the Consumer Secret displayed when the application was created.

[Previous](../marketo.md)