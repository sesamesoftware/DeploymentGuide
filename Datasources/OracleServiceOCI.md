<a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

# Oracle Service OCI

[[Installation](../guides/installguide.md)] [[Registration](../guides/RegistrationGuide.md)] [[Configuration](../guides/configurationGuide.md)] [[Datasource](../guides/DatasourceGuide.md)]

---

### *Required Information*

* **Host**
* **Database**
* **Schema**
* **Port**
* **User Name**
* **Password**

### Steps

1. From the front page of the RJ UI, go to the left hand side and click **Datasources --> New Datasource**
2. On the next screen, choose a label for your Datasource.
   1. Recommended: ``Source Oracle Service OCI`` or something similar.
   2. Select OracleServiceOCI Template
   3. Click Save
   ![Oracle Service OCI](../images/oracleserviceoci.png)
3. Logon Information Section
   1. Host
      1. IP or URL of your Oracle Service OCI.
   2. Database
      1. Your Oracle Service name.
   3. Schema
      1. Typically the same as database username
      2. Typically requires all uppercase.
   4. Port
      1. Required port, default for Oracle is 1521.
   5. Username
      1. Login name for database user.
   6. Password
      1. Password for database user.
4. If Datasource is being use as a source
   1. Date fields
      1. This is a comma separated list of fields that contain dates for use in incremental downloads
      2. Choose any and all date fields in the Schema that are altered during a create or update of the records
      3. The order of precedence is from left to right in what date field is chosen. given a date field list `LastModifiedDate, CreatedDate` when the tables is queried it will see first if `LastModifiedDate` exists if it does use that for incremental. If it doesn't then it will use `CreateDate` if neither exist it will do a full table pull.
   2. First Record Date
      1. The oldest date found in the schema for the fields in the date field list. This helps to avoid slow startup of initial load will it queries empty time.
5. Click Test
6. Once you see Connection Test Successful, click Save and Close.

---

[[&#9664; Datasource Guide](../guides/DatasourceGuide.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
