 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

[comment]: # (Change Heading to reflect Datasource)

# Sugar CRM

[comment]: # (Leave Nav BAR untouched)

[[Installation](../guides/installguide.md)] [[Registration](../guides/RegistrationGuide.md)] [[Configuration](../guides/configurationGuide.md)] [[Datasource](../guides/DatasourceGuide.md)]

---

[comment]: # (Leave Or Alter Required info as needed)

### *Required Information*

* **URL**
* **User**
* **Password**
* **First Record Date**

### Steps

[comment]: # (step 1 is common to all Datasources)
[comment]: # (Step 2.1and 2.2 should be adjusted for Data Source specific)
[comment]: # (Step 3 should be Image of the datasource you can add the screenshot to the images folder or create a placeholder like {image of datasource screen})
[comment]: # (adjust step 4 and below as needed)

1. From the front page of the RJ UI, go to the left hand side and click **Datasources &rarr; New Datasource**
2. On the next screen, choose a label for your Datasource.
   1. Recommended: ``Source SugarCRM`` or something similar.
   2. Select SugarCRM Template
   3. Click Save
   ![SugarCRM Datasource](../images/sugarcrm.png)
3. Logon Information Section
   1. URL 
      1. Example: ```https://YOUR_COMPANY_ID.sugarcrm.com```
   2. User
      1. Your SugarCRM username.
   3. Password
      1. Password for your SugarCRM user.
   4. First Record Date
      1. Date of first record. Default is set at 1970-01-01.
4. If the Datasource is being use as a source:
      1. Date fields
         1. This is a comma separated list of fields that contain dates for use in incremental downloads.
         2. Choose any and all date fields in the Schema that are altered during a create or update of the records.
         3. The order of precedence is from left to right in what date field is chosen. Given a date field list `LastModifiedDate, CreatedDate` when the tables is queried it will check first if `LastModifiedDate` exists if it does, it will use that for incremental. If it doesn't then it will use `CreateDate`. If neither exist it will do a full table pull.
      2. First Record Date
         1. The oldest date found in the schema for the fields in the date field list. This helps to avoid slow startup of initial load where it will query empty time.
5. Click Test
6. Once you see Connection Test Successful, click Save and Close.

---

[[&#9664; Datasource Guide](../guides/DatasourceGuide.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
