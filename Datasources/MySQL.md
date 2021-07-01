<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

[comment]: # (Change Heading to reflect Datasource)

## Datasource Guide for MySQL

[comment]: # (Leave Nav BAR untouched)

[Pre-Installation](../README.md)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Installation](../guides/installguide.md)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Registration](../guides/RegistrationGuide.md)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Configuration](../guides/configurationGuide.md)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Datasource](README.md)

---
[comment]: # (Leave Or Alter Required info as needed)

### *Required Information*

* **Host**
* **User Name**
* **Password**
* **Schema**
* **Port**

### Steps

[comment]: # (step 1 is common to all Datasources)
[comment]: # (Step 2.1 and 2.2 should be adjusted for Data Source specific)
[comment]: # (Step 3 should be Image of the datasource you can add the screenshot to the images folder or create a placeholder like {image of datasource screen})
[comment]: # (adjust step 4 and below as needed)

1. From the front page of the RJ UI, go to the left hand side and click **Datasources --> New Datasource**
2. On the next screen, choose a label for your Datasource. 
   1. Recommended: ‘Source MySQL’ or something similar.
   2. Select MySQL Template
   3. Click Save
3. ![MySQL Datasource](../images/MySQL.png)
4. Logon Information Section
   1. Host: *ip or dns of database server*
   2. Database: *ServiceName*
   3. Schema: *Usually the same as database Username typically uppercase*
   4. Port: *default port for oracle is 1521*
   5. Username: *login name for database user*
   6. Password: *Password for database user*
   7. tablespace: if applicable
      1. Data Tablespace
      2. Index Tablespace
      3. LOB Tablespace
5. Click Test
   1. If you see Connection Test Successful
6. if Datasource is being use as a source
   1. Date fields
      1. this is a comma separated list of fields tht contain dates for use in incremental downloads
      2. choose any and all date fields in the Schema that are altered during a create or update of the records
      3. The order of precedence is from left to right in what date field is chosen. given a date field list `LastModifiedDate, CreatedDate` when the tables is queried it will see first if `LastModifiedDate` exists if it does use that for incremental. If it doesn't then it will use `CreateDate` if neither exist it will do a full table pull.
   2. First Record Date
      1. the oldest date found in the schema for the fields in the date field list. This helps to avoid slow startup of initial load will it queries empty time.
7. click Save and Close.
[![Previous](../images/Left_Arrow_Previous.png)](README.md)