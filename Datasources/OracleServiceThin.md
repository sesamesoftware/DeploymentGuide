<a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

# Datasource Guide for Oracle Service Thin

[[Installation](../guides/installguide.md)] [[Registration](../guides/RegistrationGuide.md)] [[Configuration](../guides/configurationGuide.md)] [[Datasource](../guides/DatasourceGuide.md)]

---

### *Required Information*

* **Host**
* **Service Name**
* **User Name**
* **Password**
* **Schema**
* **Port**

### Steps

1. From the front page of the RJ UI, go to the left hand side and click **Datasources --> New Datasource**
2. On the next screen, choose a label for your Datasource.
   1. Recommended: ‘Source NetSuite’ or something similar.
   2. Select OracleServiceThin Template
   3. Click Save
3. ![Oracle Service Thin](../images/oracleservicethin.png)
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
[Datasource Guide](../guides/DatasourceGuide.md)
