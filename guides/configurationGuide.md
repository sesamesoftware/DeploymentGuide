<img  src="images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="images/RJOrbitLogo-2021Final.png" width="100">

# Relational Junction Configuration Guide

---


## Relational Junction Global Settings

Use these instructions to set up email notifications if desired. Go to Connection Configuration to skip this step.

---

## RJ Warehouse Oracle Datasource Setup

* From the front page of the RJ UI, go to the left hand side menu and click **Datasources &rarr; New Datasource**
* On the next screen, choose a label for your Datasource.  
  * *Recommendation: it should be meaningful like ‘Oracle Target for Netsuite’ or 'source Netsuite'. Setting your naming Convention from the start will save time in the future and making it quick and easy to find elements later*
* Select Template for the Technology you are connecting too
* Click Save

*Use [Datasource Guide](../Datasources/README.md) for specific guides to datasource templates*

Repeat above for source and Target. If you are using Columnar based systems like Snowflake, Redshift as your target we recommend having a metadata datasource for the transactional tables our product creates. This would need to be a row based system but can be a small db  like mysql or sql express.

---

## RJ Warehouse Datasource Connection Configuration

* From the front page of the RJ UI, go to the left hand side menu and click **Warehouse &rarr; New Config**
* Provide a name for the new configuration
  * The name should be meaningful
  * contains no spaces
* Click Create New Config

Database Connection Section
Source Datasource (select in drop down DS from 17.3.3)
Target Datasource (select in drop down DS from 17.2.1)
Metadata Datasource (select in drop down DS from 17.2.1)
Database Design Section
Verify Objects Downloaded is set to Restricted.
Leave rest as default.
Click Save and close tab.

---

## RJWarehouse Job Setup

From the front page of the RJ UI, go to the left hand side and click “Jobs”
Click New Job
The “ETL Job Label” will be the name of the job.
Click Save.
**Details tab**
On the following screen you will see 3 tabs. Details, Job Steps and History.
On the Details tab, fill out the following fields:
Schedule Id
This ID is the unique identifier for this job and will be important if you run any ETL jobs through the terminal.
Log
**Job Steps tab**
Replication Type (select in drop down **RJ Warehouse**) no email to unless they have the smtp
Replication Config (select in dropdown the config - step 4.1)
Click Add New button
Replication Step Label (Customer Choice - Suggest getGlobal)
Replication Step Type (select in dropdown **RJ Warehouse**)
Replication Step Config (select in dropdown config from step 4.1)
Replication Step Command
Field should now contain 'RJWarehouse -config [ConfigFrom4.1]'
At the end of the string, hit space and type '-getGlobal'
Tick Add to current steps box
Click Save or Save and Run
If running a job, return to the main Jobs tab to verify the job is running.

---

[Back to Install](../guides/configurationGuide.md)[Back to Main](../README.md)
