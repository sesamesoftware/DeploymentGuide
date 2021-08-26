<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

[comment]: # (Change Heading to reflect Datasource)

## Datasource Guide for Bullhorn CRM

[comment]: # (Leave Nav BAR untouched)

[![Pre-Installation](../images/Button_PreInstall.png)](guides/installguide.md)[![Installation](../images/Button_Installation.png)](guides/installguide.md)[![Registration](../images/Button_Registration.png)](guides/RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](guides/configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](README.md)

---
[comment]: # (Leave Or Alter Required info as needed)

### *Required Information*

* **Data Center Code**
* **OAuth Client ID**
* **OAuth Client Secret**

### Steps

[comment]: # (step 1 is common to all Datasources)
[comment]: # (Step 2.1and 2.2 should be adjusted for Data Source specific)
[comment]: # (Step 3 should be Image of the datasource you can add the screenshot to the images folder or create a placeholder like {image of datasource screen})
[comment]: # (adjust step 4 and below as needed)

1. Before you begin, please read and obtain the required connection information from the following document:
   1. [Bullhorn Credentials](additionalinfo/BullhornCreds.md)
2. From the front page of the RJ UI, go to the left hand side and click **Datasources &rarr; New Datasource**
3. On the next screen, choose a label for your Datasource.
   1. Recommended: `Source Bullhorn` or something similar.
   2. Select Bullhorn Template
   3. Click Save
![Bullhorn Datasource](../images/bullhorn.png)
3. Logon Information Section
   1. Data Center Code
      1. The data center code where your account's data is hosted.
      2. Example: `CLS2`, `CLS5` etc.
   2. OAuth Client ID
      1. The client ID assigned when you register your application with an OAuth authorization server.
   3. OAuth Client Secret
      1. The client secret assigned when you register your application with an OAuth authorization server.
4. If the Datasource is being used as a source:
   1. Date Fields
      1. This is a comma separated list of fields that contain dates for use in incremental downloads.
      2. Choose any and all date fields in the Schema that are altered during a create or update of the records.
      3. The order of precedence is from left to right in what date field is chosen. Given a date field list `LastModifiedDate, CreatedDate` when the tables is queried it will check first if `LastModifiedDate` exists if it does, it will use that for incremental. If it doesn't then it will use `CreateDate`. If neither exist it will do a full table pull.
   2. First Record Date
      1. The oldest date found in the schema for the fields in the date field list. This helps to avoid slow startup of initial load where it will query empty time.
5. Click Test
6. Once you see Connection Test Successful, click Save and Close.

*Note: If this is a new datasource you will be presented with a Bullhorn login screen in order to complete the authentication process.*

---

[[&#9664; Datasource Guide](../guides/DatasourceGuide.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
