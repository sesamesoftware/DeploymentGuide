<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

# Relational Junction Configuration Guide

[![Pre-Installation](../images/Button_PreInstall.png)](../README.md)[![Installation](../images/Button_Installation.png)](installguide.md)[![Registration](../images/Button_Registration.png)](RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](../Datasources/README.md)

---

## Relational Junction Global Settings

Use these instructions to set up email notifications if desired. Go to Connection Configuration to skip this step.

## RJ Warehouse Oracle Datasource Setup

1. From the front page of the RJ UI, go to the menu on the left and click **Datasources &rarr; New Datasource**
2. On the next screen, choose a label for your Datasource.
   1. *Recommendation: it should be meaningful like ‘Oracle Target for Netsuite’ or 'Source Netsuite'. Setting your naming Convention from the start will save time in the future and making it quick and easy to find elements later*
3. Select Template for the Technology you are connecting too
4. Click Save

*Use [Datasource Guide](../Datasources/README.md) for specific guides to datasource templates*

Repeat above for source and target. If you are using Columnar based systems like Snowflake, Redshift as your target we recommend having a metadata datasource for the transactional tables our product creates. This would need to be a row based system but can be a small database like mySQL or SQL express.

## RJ Warehouse Datasource Connection Configuration

1. From the front page of the RJ UI, go to the menu on the left and click **Warehouse &rarr; New Config**
2. Provide a name for the new configuration
   1. The name should be meaningful
   2. Cannot contain spaces.
3. Click Create New Config
4. { Image of database connection section}
5. Database Connection Section
   1. Source Datasource
      * The datasource you created for your Source.
   2. Target Datasource
      * The datasource you created for your Target.
   3. Metadata Datasource
      * Same as Target unless indicated otherwise.
6. { Image of database connection section}
7. Database Design Section
   1. Verify Objects Downloaded is set to Restricted.
   2. Leave rest as default.
8. Click Save
9. Close tab.

## RJWarehouse Job Setup

1. From the front page of the RJ UI, go to the menu on the left and click **Jobs &rarr; New Job**
2. The “ETL Job Label” will be the name of the job.
3. Click Save.
4. On the following screen you will see 3 tabs. Details, Job Steps and History.
{image of details tab}
   1. **Details tab**
      1. Job Label
      2. Schedule Id
         * This ID is the unique identifier for this job and will be important if you run any ETL jobs through the terminal.
      1. Schedule Job
         * [Schedule Guide](Schedule.md)
      2. Global Email Settings
         * Insert Link to Global Settings Doc.
      3. Error Notifications To
         * Email where error logs should be sent if using the Global Email Settings.
   1. {img of job steps tab}
   2. **Job Steps tab**
      1. Source Datasource
         * Select the Source Datasource you created.
      2. Target Datasource
         * Select the Target Datasource you created.
      3. Replication Type
         * Select in drop down **RJ Warehouse**.
      4. Replication Config
         * Select in dropdown the config you created.
      2. Click Add New button
      3. Replication Step Label
         * Give the step a name. Suggested: getGlobal
      1. Replication Step Type
         * Select in dropdown **RJ Warehouse**.
      1. Replication Step Config
         * Select in dropdown config you created.
      1. Replication Step Command
          * Field should now contain 'RJWarehouse -config [configfromstep8]'
          * At the end of the string, hit space and type ```-getGlobal```
      1. Tick Add to current steps box
1. Click Save or Save and Run
   * If running a job, return to the main Jobs tab to verify the job is running.

[Back to Install](../guides/configurationGuide.md)
[Back to Main](../README.md)
