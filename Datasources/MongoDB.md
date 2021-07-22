 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

[comment]: # (Change Heading to reflect Datasource)

#  MongoDB ERP

[comment]: # (Leave Nav BAR untouched)

[[Installation](../guides/installguide.md)] [[Registration](../guides/RegistrationGuide.md)] [[Configuration](../guides/configurationGuide.md)] [[Datasource](../guides/DatasourceGuide.md)]

---

[comment]: # (Leave Or Alter Required info as needed)

### *Required Information*

* **Server**
* **Database**
* **Schema**
* **Port**
* **User**
* **Password**

### Steps

[comment]: # (step 1 is common to all Datasources)
[comment]: # (Step 2.1and 2.2 should be adjusted for Data Source specific)
[comment]: # (Step 3 should be Image of the datasource you can add the screenshot to the images folder or create a placeholder like {image of datasource screen})
[comment]: # (adjust step 4 and below as needed)

1. From the front page of the RJ UI, go to the left hand side and click **Datasources --> New Datasource**
2. On the next screen, choose a label for your Datasource.
   1. Recommended: ‘Source MongoDB' or something similar.
   2. Select MongoDB Template
   3. Click Save
   ![MongoDB Datasource](../images/MongoDB.png)
3. Logon Information Section
   1. Server
   2. Database: *MongoDB Name*
   3. Schema: *Database schema, use % if unknown.*
   4. Port: *Default 27017*
   5. User: *Login name for database user*
   6. Password: *Password for database user*
   7. AuthMechanism: *Auth mechanism that Mongo will use to authenticate the connection.*
      1. SCRAM-SHA-1
      2. SCRAM-SHA-256
      3. PLAIN
      4. GSSAPI
   8. AuthDatabase *Name of Mongo database used for authentication.* 
   9. RowScanDepth: *The maximum number of rows to scan to look for the columns available in a table. Set this property to  gain more control over how the provider applies data types to collections; default 100*
   10. SlaveOK: *Whether provider is allowed to read from secondary servers; default FALSE.*
   11. ReadPreference: *Accepted values are primary, primaryPreferred, secondary, secondaryPreferred, and nearest.*
   12. ReplicaSet: *Specify multiple servers in addition to the one configured in Server and Port. Specify server name and port; separate servers with a comma.*
   13. Batch Mode
   14. Batch Size *Default 200*
   15. First Record Date *Default 1970-01-01*
   16. Date Fields *See below*
   17. Schema Prefix Case: *UPPER/LOWER, if required.*
   18. Tablename Case: *UPPER/LOWER, if required.*
   19. Select Fields
       1.  FIELD_LIST
       2.  STAR
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