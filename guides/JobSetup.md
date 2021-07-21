 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

#  Job Configuration - Setup

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

1. From the front page of the RJ UI, go to the menu on the left and click **Jobs &rarr; New Job**
2. The “ETL Job Label” will be the name of the job.
3. Click Save.

#### Details Tab

![Details Tab](../images/jobsteps2.png)
1. Job Label
2. Schedule Id
   1. This ID is the unique identifier for this job and will be important if you run any ETL jobs through the terminal.
3. Schedule Job
   1. [Schedule Guide](./Supporting/Schedule.md)
4. Global Email Settings
   1. Insert Link to Global Settings Doc.
5. Error Notifications To
   1. Email where error logs should be sent if using the Global Email Settings.

#### Job Steps Tab

![Job Steps Tab](../images/jobsteps3.png)

1. Source Datasource
   1. Select the Source Datasource you created.
2. Target Datasource
   1. Select the Target Datasource you created.
3. Replication Type
   1. Select in drop down RJ Warehouse.
4. Replication Config
   1. Select in dropdown the config you created.
5. Click Add New button
6. Replication Step Label
   1. Give the step a name. 
   2. Suggested: getGlobal
7. Replication Step Type
   1. Select in dropdown RJ Warehouse.
8. Replication Step Config
   1. Select in dropdown config you created.
9. Replication Step Command
   1.  Field should now contain 'RJWarehouse -config [configfromStep8]
   2.  At the end of the string, hit space and type ```-getGlobal```
10. Tick Add to current steps box
11. Click Save or Save and Run
12. If running a job, return to the main Jobs tab to verify the job is running.

---

 [[&#9664; Create Warehouse Config](rjwarehouseconfig.md)] [[Back to Main &#9654;](../README.md)]

 <p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
