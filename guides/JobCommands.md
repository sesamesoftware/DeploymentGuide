 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

# Job Configuration - Commands

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

## Job Commands

Options:
-config [config suffix] Use rjwarehouse.properties file suffix
-getSchema [object] Sync database schema with Source and print tabbed report
-getSchemaGlobal Sync database with entire Source Schema and print tabbed report
-getSchemaTabbed [object] Sync database schema with Source schema and print tabbed report
-getSchemaTabbedGlobal Sync database schema with entire Source schema and print tabbed report
-get [object] Download records of an object, automatic full load or incremental
-getGlobal Download Updated records of all objects if there is recent history
-getParallelGlobal Download Updated records of all objects if there is recent history, processing multiple objects simultaneously
-getIndex [object] Create foreign key indexes for one object
-getIndexGlobal Create foreign key indexes for all objects
-getReference [object] Create poplist metadata for one object
-getReferenceGlobal Create poplist metadata for all objects
-set [object] Upload records of an object to Salesforce
-setGlobal Upload records of a set of objects to Salesforce
-checkGlobal Check -setGlobal to see if the objects are listed in order of their hierarchical order so parents load first
-checkSchema [object] Check Source object against database schema
-checkSchemaGlobal Check all Source objects against database schema
-checkExclude [object] Run a 'checkExclude' on this [object]
-checkExcludeGlobal Run a 'checkExclude' for all available Saleforce objects
-audit [object] Validate missing, changed, and un-deleted records for an object
-auditGlobal Validate missing, changed, and un-deleted records for all objects
-pause [delay (seconds)] Program will sleep for 'delay' seconds
-reset [object] Remove all replication history for an object to enable full refresh
-resetGlobal Remove all replication history for all objects to enable full refresh
-purgeDeleted [object] Remove all records for an object That has a Delete flag of Y
-purgeDeletedGlobal Remove all records for all objects That has a Delete flag of Y
-dropTable [object] Drop target database table for the given source object
-dropTableForce [object] Drop database table without Source Integrity Check
-dropTableGlobal Drops all Tables in the configured database including RJ meta tables
-dropColumn [object] [field] Drop column from database table for a given source object
-dropColumnForce [object] [field] Drop column from database table without Source Integrity Check
-dropIndex [Object] Drops all Indexes in the configured database against the Object
-dropIndexGlobal Drops all Indexes in the configured database against all Objects
-clean Delete work, log, and export files
-truncate [object] Delete all rows in a table
-truncateGlobal Delete all rows in all tables in the RJ Objects Table
-getParallel [object] Splits a download in to separate stacks in memory and download data at the same time
-createForeignKeyGlobal Creates inactive foreign key constraints in the target DBMS. The RJ_OBJECT_RELATIONSHIP table must first be populated with a -getSchemaGlobal command
-dropForeignKeyGlobal Drops all RJWarehouse created foreign key constraints in the target DBMS
-getFileCabinet Download the file cabinet files to the OS. Depends on first running -get folder and then -get file first


---

[[&#9664; Create Datasources](DatasourceGuide.md)] [[create and Run Job &#9654;](JobSetup.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>