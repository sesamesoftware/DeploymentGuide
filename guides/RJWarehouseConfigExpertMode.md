 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

# Warehouse Configuration - Expert Mode

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

At the top of your configuration, select the radial button for Expert Mode.

![AdvancedConfigProps](../images/advconfigprop1.png)

#### Database Design:

1. Maximum VARCHAR Size
   1. This value is used to determine if a CLOB or TEXT data type will be used. If the length is greater than this value a CLOB or TEXT data type will be used.  This will affect the ability to store large rows in a given table, since CLOB or TEXT fields are typically not stored in the same physical record and do not count against the block size limit. If “use internationalization” is set to true, you cannot set this higher than 2000. If use internationalization is set to false, you cannot set this higher than 4000. If you are using a DBMS like MySQLor Maria DB you will not want to set this higher than 255 due to database limitations.
   
2. Database Partitioning (Yes | No)
   1. Default No.
   2. Whether this is a DB2 partitioned database or not.
   
3. Table Prefix (True | False)   
   1. Use a prefix of “T” for all table names. This can be set to any legal value, or omitted to use non-prefixed names.
   2. For readability it is recommended that with the use of the prefix and an underscore to the end of the prefix for something like ```SF_```  ```NS_``` or ```T_``` this will result in a bit of visual separation when looking at the tables. 
   3. If you do not use a table prefix then tables that are DBMS reserved words will have an X appended to the end of the table name.
   
4. Custom Field Suffix (Yes | No)
   1. Default Yes.
   2. Allow Table and column names for custom fields to retain the “__C” suffix.
   
5. DBMS-Independent Names (Yes | No)
   1. Default Yes.
   2. 
      1. Yes
         1. 
   3. With this set to true it will check database names against all supported DBMS reserved word lists. Use this option to improve cross-platform compatibility. With it set to false it will only check database names against the reserved words file for that database. For instance, NAME will become NAMEX. It is not recommended that you change this setting to false if you are transferring data across different database versions.
   
6. Custom Formula Fields
   1. Most DBMS platforms will not accept insert or updates if the record does not fit into a single database block. This is not an issue for Oracle. DB2 will not even let you create the column if there is even a potential to exceed the block size. This option turns off creation and replication of all custom formula fields. This also ensures that reports do not represent out of date information if the formula is based on date-sensitive computations. Must be turned on to replicate custom formula fields.
   
7. Objects Downloaded
   1. Restricted 
      1. Use this option to control which tables are downloaded. The objects must exist in the datasource and the user must have access to the objects. Objects cannot be in both the download and exclude config.
   2. Unrestricted (Default) 
      1. This option will attempt to download all tables from the datasource unless they are in the exclude config or default exclude config file. Use this to get started or if you want the system to download all tables automatically. You can create a download config file to define the initial order of the objects in the download and then the rest of the tables will be downloaded in a mostly alphabetical order. Package objects are sometimes presented out of alphabetical order.
   3. Objects cannot be in both the download and exclude config. See the document [Select Table to Load](RJWarehouseConfigSelectTables.md) for more information.

8. Objects Uploaded
   1. Restricted 
      1. Use this option to control which tables are uploaded. The objects must exist in the datasource and the user must have access to the objects. Objects need to be in a parent child relational order or else you can get errors like invalid cross reference id. Objects cannot be in both the upload and exclude config.
   2. Unrestricted (Default) 
      1. This option will attempt to download all tables from datasource unless they are in the exclude config or default exclude config file. Use this to get started or if you want the system to download all tables automatically. You can create a download config file to define the initial order of the objects in the download and then the rest of the tables will be downloaded in a mostly alphabetical order. Package objects are sometimes presented out of alphabetical order.
   3. Objects cannot be in both the download and exclude config. See the document [Select Table to Load](RJWarehouseConfigSelectTables.md) for more information.

Note: Even if your configuration file is set to restricted mode you can still download or upload a specific object using one of the single object commands.
   
9.  Auto Adjust Column Width
    1.  Optional parameter to turn off the automatic size adjustment of VARCHAR/NVARCHAR columns. 
    2.  True (Default)
        1.  RJ will automatically adjust column widths. 
    3.  False
        1.  If the schema is modified and this option is false, a message will appear in the log indicating that the field is smaller than the datasource metadata indicates. This can cause records to be rejected if the data does not fit the column width.  RJ will only increase the size of a field it will not decrease the field size. You would have to drop the column and rebuild it to have it reduced in size.
10. System of Record
    1.  This is used to determine which source wins out on a download when a change has been made to records in the local database in preparation to upload to the datasource.
    2.  Datasource (Default)
        1.  When you change records in the database in preparation to send to datasource and a download happens first if the record has changed in the datasource it will overwrite the data in the database.
    3.  Local
        1.  When you change records in the database in preparation to send to datasource and a download happens first if the record has changed in datasource the data in the database will not be overwritten as long as their delete_flag is set to any one of the action flags or action flag errors.

The order of operation when it comes to the job steps can also be used to determine the system of record when the setting is set to datasource. Doing a -set then a -get (local db is system of record)  vs doing a -get then a -set (datasource is system of record).; default datasource

1.   Download Config:  
     1.   The name of the file in the RJ_HOME\1000\rjwarehouse\conf directory containing the object names in order to be downloaded for download operations. The default config file is download.config. You can specify different user created config files and place them in this setting. If the datasource config file is set to restricted mode then even if you run a single object command you still have to have the object listed in the download.config file that you are using; default download.config
    
2.  Upload Config: 
    1.  Upload Config The name of the file in the RJ_HOME\1000\rjwarehouse\conf directory containing the object names in order to be uploaded in upload operations. The default config file is upload.config.You can specify different user created config files and place them in this setting. If the datasource config file is set to restricted mode then even if you run a single object command you still have to have the object listed in the upload.config file that you are using. default upload.config
    
3.  Exclude Config: 
    1.  Exclude Config The name of the file in the RJ_HOME\1000\rjwarehouse\conf directory containing the objects to be ignored download or upload operations. The default config file is exclude.config. You can specify different user created config files and place them in this setting.
    2.  Note: By default the download, upload, and exclude configs are already populated with some standard objects.  Upon initialization, a checkExcludeGlobal will run creating an exclude.config.default file looking at the current datasource object list and verifying which objects are usable or not.  This file will reside in the RJ_HOME\1000\rjwarehouse\conf folder. You can create user specific object config files by using the select tables to load tab. exclude.config

4.  Track History: 
    1.  Track History (true | false). Whether history tables will be generated. If true, the prior images of any changed record will be recorded in a corresponding history table. These tables will be created with an X prefix. For example the account table will have a corresponding xaccount table.

5.   Use Internationalization (Unicode): Y/N 
     1.   This setting is to be used for unicode characters. Due to changes in the functioning of datasource they have added the ability to have multiple different types of unicode data including emoticons. It will create NVARCHAR or equivalent data types for most all fields capable of having unicode data. By default this setting is set to true and should not be changed unless 100% sure there will never be any unicode data present in any of your objects.

6.  Database Genesis: 
    1.  Database Genesis: The start date for the database data. Can be a year (2000) or date (2000-12-01). If empty, defaults to 1970-01-01. 2005-01-01
    
7.  Bulk Loader Error Limit: 	
    1.  Bulk Loader Error Limit: Max errors for bulk loader to throw before termination.

8.  Bulk Loader escape character: 	
    1.  Bulk Loader Escape Character: Escape character to use in flat file construction.

9.  Truncate Error Table Objects: 
    1.  Truncate Error table objects: This option does not currently do anything as an automatic feature is enabled and is scheduled to be removed from the UI. see  rj.logging.rejectLevel Yes

10. Maximum Byte Count: 	
    1.  Maximum Byte Count: Data is monitored for the given day (i.e. midnight to midnight) if the total bytes in the day exceed the maxByteCount property then the program shuts down with the appropriate error. Value is in GB.


---

[[&#9664; Create Datasources](DatasourceGuide.md)] [[create and Run Job &#9654;](JobSetup.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>