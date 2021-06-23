<img src="../images/SesameSoftwareLogo-2020Final.png" width="200"><img src="../images/RJOrbitLogo-2021Final.png" width="200">

## Datasource Guide for Oracel Service Thin

##### *Required Information*

* **Host**
* **Service Name**
* **User Name**
* **Password**
* **Schema**
* **Port**

##### *Steps*
1. From the frontpage of the RJ UI, go to the left hand side and click **Datasources --> New Datasource**
2. On the next screen, choose a label for your Datasource. 
   1. Recommended: ‘Source NetSuite’ or something similar.
   2. Select OracleServiceThin Template
   3. Click Save
3. Logon Information Section
   1. Host: *ip or dns of databse server*
   2. Database: *ServiceName*
   3. Scheama: *Usually the same as database Username typically uppercase*
   4. Port: *default port for oracel is 1521*
   5. Username: *login name for databaseuser*
   6. Password: *Password for database user*
   7. tablespace: if applicable
      1. Data Tablespace
      2. Index Tablespace
      3. LOB Tablesapce
4. Click Test
   1. If you see Connection Test Successful
5. if Datasource is being use as a source
   1. Date fields
      1. this is a comma seperated list of fields tht contain dates for use in incremental downloads
      2. choose anay and all datefields in the Schema that are altered during a create or update of the records
      3. The order of prescidence is from left to right in what dat is choosen. given a date field list `LastModifiedDate, CreatedDate` when the tables is queried it will see first if `LastModifiedDate` exists if it does use that for incremental. If it doesn;t then it will use `CreateDate` if neither exist it will do a full table pull.
   2. First Record Date
      1. the oldest date found in the schema for the fields in the datefield list. This helps to avoid slow startup of inital load will it queries empty time.
6. click Save and Close.
