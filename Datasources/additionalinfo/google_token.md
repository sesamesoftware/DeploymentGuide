 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

[comment]: # (Change Heading to reflect Datasource)

# Google Oauth Token

[comment]: # (Leave Nav BAR untouched)

[[Installation](../guides/installguide.md)] [[Registration](../guides/RegistrationGuide.md)] [[Configuration](../guides/configurationGuide.md)] [[Datasource](../guides/DatasourceGuide.md)]

---

[comment]: # (Leave Or Alter Required info as needed)

### *Generate a New Token*

Google Analytics uses custom OAuth2 to authenticate Google Analytics.  A service account OAuthAccessToken is used to authenticate.  The token cannot be seen anywhere in Google, but can be recreated, and the file containing the keys can be downloaded if a new key is created.

### Steps

[comment]: # (step 1 is common to all Datasources)
[comment]: # (Step 2.1and 2.2 should be adjusted for Data Source specific)
[comment]: # (Step 3 should be Image of the datasource you can add the screenshot to the images folder or create a placeholder like {image of datasource screen})
[comment]: # (adjust step 4 and below as needed)

1. Login to Google Cloud Console.
2. Go to API’s and Services &rarr; Credentials.
3. Create Credentials &rarr; Create new Service Account.
4. Download the file generated with the service account credentials.
5. The private key is used for the Oauth Access Token. Copy the key starting after ---\n to before the \n at the end of the field, and enter the value in the OAuthAccessToken.

---

[[&#9664; Google Analytics Datasource Guide](Datasources\GoogleAnalytics.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../../images/poweredBy.png" height="80px"></img></a> </p>
