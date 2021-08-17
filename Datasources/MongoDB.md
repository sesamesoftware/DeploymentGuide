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

1. Access is restricted by IP address. Before you begin, verify that your IP address is whitelisted in the Network Access tab of your MongoDB UI.
2. From the front page of the RJ UI, go to the left hand side and click **Datasources --> New Datasource**
3. On the next screen, choose a label for your Datasource.
   1. Recommended: ‘Source MongoDB' or something similar.
   2. Select MongoDB Template
   3. Click Save
   ![MongoDB Datasource](../images/MongoDB.png)
4. Logon Information Section
   1. Server
      1. Hostname/IP of server with your MongoDB Database.
   2. Database
      1. Name of the database to replicated.
      2. Located in the Databases tab of your MongoDB UI.
   3. Schema
      1. Your database schema name, use % if unknown.
   4. Port
      1. Required port, default is 27017.
   5. User
      1. Username login.
   6. Password
      1. Password for the user login.
   7. AuthMechanism: 
      1. Choose your authentication method.
      2. You can locate this information in the Database Access tab of your MongoDB UI.
   8. AuthDatabase 
      1. Enter the name of Mongo database used for authentication.
      2.  2. You can locate this information in the Database Access tab of your MongoDB UI.
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