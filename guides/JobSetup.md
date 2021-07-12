[![Logo](../images/SesameLogo110x110.png)](http://www.sesamesoftware.com) <img align=right src="../images/RJOrbit110x110.png">

## RJWarehouse Job Setup

[![Installation](../images/Button_Installation.png)](installguide.md)[![Registration](../images/Button_Registration.png)](RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](DatasourceGuide.md)

---

1. From the front page of the RJ UI, go to the menu on the left and click **Jobs &rarr; New Job**
2. The “ETL Job Label” will be the name of the job.
3. Click Save.
4. On the following screen you will see 3 tabs. Details, Job Steps and History.
{image of details tab}
   1. **Details tab**
      1. Job Label
      2. Schedule Id
         * This ID is the unique identifier for this job and will be important if you run any ETL jobs through the terminal.
      3. Schedule Job
         * [Schedule Guide](Schedule.md)
      4. Global Email Settings
         * Insert Link to Global Settings Doc.
      5. Error Notifications To
         * Email where error logs should be sent if using the Global Email Settings.

{img of job steps tab}

   1. **Job Steps tab**
      1. Source Datasource
         * Select the Source Datasource you created.
      2. Target Datasource
         * Select the Target Datasource you created.
      3. Replication Type
         * Select in drop down **RJ Warehouse**.
      4. Replication Config
         * Select in dropdown the config you created.
      5. Click Add New button
      6. Replication Step Label
         * Give the step a name. Suggested: getGlobal
      7. Replication Step Type
         * Select in dropdown **RJ Warehouse**.
      8. Replication Step Config
         * Select in dropdown config you created.
      9. Replication Step Command
          * Field should now contain 'RJWarehouse -config [configfromstep8]'
          * At the end of the string, hit space and type ```-getGlobal```
      10. Tick Add to current steps box
   1. Click Save or Save and Run
   1. If running a job, return to the main Jobs tab to verify the job is running.

 [[Create Warehouse Config](rjwarehouseconfig.md)] [[Back to Main](../README.md)]
