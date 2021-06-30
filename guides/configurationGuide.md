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
   2. contains no spaces
3. Click Create New Configuration
4. { Image of database connection section}
5. Database Connection Section
   1. Source Datasource (select in drop down DS from 17.3.3)
   2. Target Datasource (select in drop down DS from 17.2.1)
   3. Metadata Datasource (select in drop down DS from 17.2.1)
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
4. On the following screen you will see 3 tabs. Details, Job Steps, and History.
5. {image of details tab}
   1. **Details tab**
      1. Schedule ID
         1. This ID is the unique identifier for this job and will be important if you run any ETL jobs through the terminal.
      2. Log
      3. no email to unless they have the STMP
      4. For Scheduling see [schedule guide](Schedule.md)
   2. {image of job steps tab}
   3. **Job Steps tab**
      1. Replication Type (select in drop down **RJ Warehouse**)
      2. Replication Config (select in dropdown the configuration - step 4.1)
      3. Click Add New button
         1. Replication Step Label (Customer Choice - Suggest getGlobal)
         2. Replication Step Type (select in dropdown **RJ Warehouse**)
         3. Replication Step Config (select in dropdown config from step 4.1)
         4. Replication Step Command
            1. Field should now contain 'RJWarehouse -config [ConfigFrom4.1]'
            2. At the end of the string, hit space and type '-getGlobal'
      4. Click 'Add to current steps box'
6. Click 'Save or Save and Run'
If running a job, return to the main Jobs tab to verify the job is running.

[Back to Install](../guides/configurationGuide.md)
[Back to Main](../README.md)
