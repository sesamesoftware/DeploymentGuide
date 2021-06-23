

Relational Junction Global Settings
Use these instructions to set up email notifications if desired. Go to Connection Configuration to skip this step.

RJ Warehouse Oracle Datasource Setup
From the frontpage of the RJ UI, go to the left hand side and click “Datasources”
Click New Datasource
On the next screen, choose a label for your Datasource. Recommended: ‘Oracle Target’ or something similar.
Select Template

Click Save
Once on the next screen, scroll to the bottom and click File Wizard.
Click Choose File
Use Wallet from OCI Instance
Click Upload
Click Close
Nessc Information
Logon Information → DB Service Name = {Database Service Name}
Logon Information → Schema = {Database Schema}
Logon Information → Username = Username
1. Password

Click Test
If you see Connection Test Successful, click Save and Close.

RJ Warehouse Source Datasource Setup
Select a link below to take you to your chosen source in the appendix.

NetSuite

RJ Warehouse Datasource Connection Configuration
From the frontpage of the RJ UI, go to the left hand side and click “Warehouse”
Click New Config
Provide a name for the new configuration (Customer Choice) - one word
Click Create New Config
Database Connection Section
Source Datasource (select in drop down DS from 17.3.3)
Target Datasource (select in drop down DS from 17.2.1)
Metadata Datasource (select in drop down DS from 17.2.1)
Database Design Section
Verify Objects Downloaded is set to Restricted.
Leave rest as default.
Click Save and close tab.

RJWarehouse Job Setup
From the frontpage of the RJ UI, go to the left hand side and click “Jobs”
Click New Job
The “ETL Job Label” will be the name of the job.
Click Save.
On the following screen you will see 3 tabs. Details, Job Steps and History.
On the Details tab, fill out the following fields:
Schedule Id
This ID is the unique identifier for this job and will be important if you run any ETL jobs through the terminal.
Log
On Job Steps tab:
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
