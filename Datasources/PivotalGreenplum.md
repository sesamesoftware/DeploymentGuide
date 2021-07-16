 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

[comment]: # (Change Heading to reflect Datasource)

#  Greenplum

[comment]: # (Leave Nav BAR untouched)

[[Installation](../guides/installguide.md)] [[Registration](../guides/RegistrationGuide.md)] [[Configuration](../guides/configurationGuide.md)] [[Datasource](../guides/DatasourceGuide.md)]

---

[comment]: # (Leave Or Alter Required info as needed)

### *Required Information*

* **Host Name**
* **Database Name**
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
   1. Recommended: ‘Source Greenplum' or something similar.
   2. Select Greenplum Template
   3. Click Save
3. {Sybase img goes here}
4. Logon Information Section
   1. Host Name: *IP or DNS of database server*
   2. Database Name:
   3. Schema: *Usually the same as database username typically uppercase*
   4. Port: *Default 5432*
   5. User: *Login name for database user*
   6. Password: *Password for database user*
   7. SSH User Name 	
   8. SSH Password 	
   9. pem Key File Location: *Location of the .pem private key file.*
   10. pem Key Pass Phrase: *Password of the pem Key file*
   11. Compression
       1.  TAR
       2.  GunZip
   12. Path to Greenplum Utilities *Location of Greenplum file.*
   13. Command list to execute
   14. Utility Host: *Host where the gpload command will be executed.*
   15. SSH Port: *Default 22*
   16. VM IP Address: *VM IP Address, default is host*
   17. Remote Directory: *Remote directory/folder where files are copied and processed*
   18. First Record Date *Default 1970-01-01*
   19. Date Fields *See below*
   20. Schema Prefix Case: *UPPER/LOWER, if required.*
   24. Tablename Case: *UPPER/LOWER, if required.*
   25. Select Fields
       1.  FIELD_LIST
       2.  STAR
   26. SSL: *Control use of SSL; any non-null value causes SSL to be required.* 
5. If the Datasource is being use as a source:
      1. Date fields
         1. This is a comma separated list of fields that contain dates for use in incremental downloads.
         2. Choose any and all date fields in the Schema that are altered during a create or update of the records.
         3. The order of precedence is from left to right in what date field is chosen. Given a date field list `LastModifiedDate, CreatedDate` when the tables is queried it will check first if `LastModifiedDate` exists if it does, it will use that for incremental. If it doesn't then it will use `CreateDate`. If neither exist it will do a full table pull.
      2. First Record Date
         1. The oldest date found in the schema for the fields in the date field list. This helps to avoid slow startup of initial load where it will query empty time.
6. Click Test
7. Once you see Connection Test Successful, click Save and Close.

---

[[&#9664; Datasource Guide](../guides/DatasourceGuide.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>