<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

## Datasource Guide for Marketo

[![Pre-Installation](../images/Button_PreInstall.png)](../guides/installguide.md)[![Installation](../images/Button_Installation.png)](../guides/installguide.md)[![Registration](../images/Button_Registration.png)](../guides/RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](../guides/configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](README.md)

---

### *Required Information*

* **RESTEndpoint** The url to the marketo rest api. 
* **Access Tokens** The OAuth Token, Client ID, and client secret generated in Marketo

### *Steps*

1. Before you begin, set up API access and obtain OAuth tokens:
   2. [OAuth Credentials](additionalinfo/MarketoCreds.md)
2. From the frontpage of the RJ UI, go to the left hand side and click **Datasources --> New Datasource**
3. On the next screen, choose a label for your Datasource.
   1. Recommended: ```Source Marketo``` or something similar.
4. Select the Marketo Template
5. ![Datasource](../images/marketo1.png)
6. Logon Information Section 
   1. RESTEndpoint
7. ![tokens](../images/marketo2.png)
8. Open Authorization Section - Authorization Tokens from Marketo
   1. Application ID Tokens
      1. OAuthAccessToken
   2. Login Tokens
      1. OAuthClientId
      2. OAuthClientSecret
9. Click Test
10. Save and Close.

[![Previous](../images/Left_Arrow_Previous.png)](README.md)
