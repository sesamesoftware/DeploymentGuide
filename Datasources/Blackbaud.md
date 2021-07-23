 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

[comment]: # (Change Heading to reflect Datasource)

#  Blackbaud FE NXT

[comment]: # (Leave Nav BAR untouched)

[[Installation](../guides/installguide.md)] [[Registration](../guides/RegistrationGuide.md)] [[Configuration](../guides/configurationGuide.md)] [[Datasource](../guides/DatasourceGuide.md)]

---

[comment]: # (Leave Or Alter Required info as needed)

### *Required Information*

* **Subscription Key**
* **OAuth Client ID**
* **OAuth Client Secret**
* **Callback URL**

### Steps

[comment]: # (step 1 is common to all Datasources)
[comment]: # (Step 2.1and 2.2 should be adjusted for Data Source specific)
[comment]: # (Step 3 should be Image of the datasource you can add the screenshot to the images folder or create a placeholder like {image of datasource screen})
[comment]: # (adjust step 4 and below as needed)

1. Before you begin, obtain:
   * [Blackbaud Credentials](additionalinfo/BlackbaudCreds.md)
2. From the front page of the RJ UI, go to the left hand side and click **Datasources --> New Datasource**
3. On the next screen, choose a label for your Datasource.
   1. Recommended: ‘Source Blackbaud’ or something similar.
   2. Select Blackbaud Template.
   3. Click Save.
![Blackbaud FE NXT Datasource](../images/blackbaud.png)
4. Logon Information Section
   1. Subscription Key: *Subscription key which provides access to the API. Found in your Profile.*
   2. OAuth Client ID: *The client ID assigned when you register your application with an OAuth authorization server.*
   3. OAuth Client Secret: *The client secret assigned when you register your application with an OAuth authorization server.*
   4. Callback URL: *The OAuth callback URL to return to when authenticating. This value must match the callback URL you specify in your app settings.*
6. If the Datasource is being used as a source:
      1. Date fields
         1. This is a comma separated list of fields that contain dates for use in incremental downloads.
         2. Choose any and all date fields in the Schema that are altered during a create or update of the records.
         3. The order of precedence is from left to right in what date field is chosen. Given a date field list `LastModifiedDate, CreatedDate` when the tables is queried it will check first if `LastModifiedDate` exists if it does, it will use that for incremental. If it doesn't then it will use `CreateDate`. If neither exist it will do a full table pull.
      2. First Record Date
         1. The oldest date found in the schema for the fields in the date field list. This helps to avoid slow startup of initial load where it will query empty time.
7. Click Test

*Note: If this is a new datasource you will be presented with a Blackbaud login screen in order to complete the authentication process.*
8. Once you see Connection Test Successful, click Save and Close.

---

[[&#9664; Datasource Guide](../guides/DatasourceGuide.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
