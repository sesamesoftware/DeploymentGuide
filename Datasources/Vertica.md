 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

[comment]: # (Change Heading to reflect Datasource)

#  Vertica

[comment]: # (Leave Nav BAR untouched)

[[Installation](../guides/installguide.md)] [[Registration](../guides/RegistrationGuide.md)] [[Configuration](../guides/configurationGuide.md)] [[Datasource](../guides/DatasourceGuide.md)]

---

[comment]: # (Leave Or Alter Required info as needed)

### *Required Information*

* **Host**
* **Database**
* **User**
* **Password** 

### Steps

[comment]: # (step 1 is common to all Datasources)
[comment]: # (Step 2.1and 2.2 should be adjusted for Data Source specific)
[comment]: # (Step 3 should be Image of the datasource you can add the screenshot to the images folder or create a placeholder like {image of datasource screen})
[comment]: # (adjust step 4 and below as needed)
<!--Host * Help	
database * Help	
Schema Help	
Port Help	
User * Help	
Password * Help	
SSH User Name Help	
SSH Password Help	
pem Key File Location Help	
pem Key Pass Phrase Help	
compression Help	
NONE
Utility Host Help	
Remote Directory Help	
SSH Port Help	
22
Batch Size Help	
500
First Record Date Help	
1970-01-01
Date Fields Help	
Schema Prefix Help	
UPPER
Tablename Case Help	
UPPER
Select Method -->

1. From the front page of the RJ UI, go to the left hand side and click **Datasources --> New Datasource**
2. On the next screen, choose a label for your Datasource.
   1. Recommended: ‘Source Vertica' or something similar.
   2. Select Vertica Template
   3. Click Save
3. {img goes here}
4. Logon Information Section
   1. Host: *IP or DNS of database server*
   2. Database:
   3. Schema: *Usually the same as database Username typically uppercase*
   4. Port:
   5. User: *login name for database user*
   6. Password: *Password for database user*
   7. SSH User Name 	
   8. SSH Password 	
   9. pem Key File Location: *Location of the .pem private key file.*
   10. pem Key Pass Phrase: Password 
   11. Compression
       1.  TAR
       2.  GunZip
   12. Utility Host: *Host where the file will be loaded*
   13. Remote Directory Help	
   14. SSH Port: *Default 22*
   15. Batch Size *Default 500*
   16. First Record Date *Default 1970-01-01*
   17. Date Fields *See below*
   18. Schema Prefix *Default UPPER*
   19. Tablename Case *Default UPPER*
1. Click Test
   1. If you see Connection Test Successful
2. If the Datasource is being use as a source
   1. Date fields
      1. This is a comma separated list of fields that contain dates for use in incremental downloads.
      2. Choose any and all date fields in the Schema that are altered during a create or update of the records.
      3. The order of precedence is from left to right in what date field is chosen. Given a date field list `LastModifiedDate, CreatedDate` when the tables is queried it will check first if `LastModifiedDate` exists if it does, it will use that for incremental. If it doesn't then it will use `CreateDate`. If neither exist it will do a full table pull.
   2. First Record Date
      1. the oldest date found in the schema for the fields in the date field list. This helps to avoid slow startup of initial load will it queries empty time.
3. Click Save and Close.

---

[[&#9664; Datasource Guide](../guides/DatasourceGuide.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
