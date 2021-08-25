 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

# Relational Junction Datasource Guide

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

## RJ Warehouse Oracle Datasource Setup

1. From the front page of the RJ UI, go to the menu on the left and click **Datasources &rarr; New Datasource**
2. On the next screen, choose a label for your Datasource.
   1. *Recommendation: The name of each job should be clear and meaningful. Setting your naming convention from the start will save time in the future and make it quick and easy to find elements later. Example: ‘Oracle Target for Netsuite’ or 'Source Netsuite'.*
3. Select Template for the Technology you are connecting to.
4. Click Save

*Use the [Datasource Guide](#supported-datasources) for specific guides to datasource templates.*

Repeat above for your source and target. If you are using Columnar based systems like Snowflake or Redshift as your target Sesame recommends having a metadata datasource for the transactional tables our product creates. This would need to be a row based system but can be a small database like mySQL or SQL express.

### Supported Datasources

* [1010DATA](../Datasources/1010data.md)
* [Amazon Aurora MySQL](../Datasources/Aurora_Mysql.md)
* [Amazon Aurora PostgreSQL](../Datasources/Aurora_Postgres.md)
* [Amazon Dynamo DB](../Datasources/DynamoDB.md)
* [Amazon Redshift](../Datasources/AmazonRedishift_Postgres.md)
* [Blackbaud](../Datasources/Blackbaud.md)
* [Bullhorn CRM](../Datasources/BullhornCRM.md)
* [Chargebee](../Datasources/Chargebee.md)
* [ConnectWise](../Datasources/Connectwise.md)
* [Couchbase](../Datasources/Couchbase.md)
* [CSV/TSV](../Datasources/CSV.md)
* [DB2](../Datasources/db2.md)
* [DB2AS400](../Datasources/db2AS400.md)
* [Google Analytics](../Datasources/GoogleAnalytics.md)
* [Google BigQuery](../Datasources/GoogleBigQuery.md)
* [Kronos](../Datasources/Kronos.md)
* [MariaDB](../Datasources/MariaDB.md)
* [Marketo](../Datasources/Marketo.md)
* [Microsoft Access](../Datasources/Access.md)
* [Microsoft Azure](../Datasources/Azure.md)
* [Microsoft Dynamics CRM](../Datasources/MSDynamicsCRM.md)
* [Microsoft Excel](../Datasources/Excel.md)
* [Microsoft MySQL](../Datasources/MySQL.md)
* [Microsoft Office365](../Datasources/Office365.md)
* [Microsoft SQL Server](../Datasources/MySQL.md)
* [Microsoft Teams](../Datasources/MSTeams.md)
* [MongoDB](../Datasources/MongoDB.md)
* [NetSuite](../Datasources/netsuite.md)
* [Oodo](../Datasources/Oodo.md)
* [Oracle Autonomous Data Warehouse](../Datasources/OracleADW.md)
* [Oracle Autonomous Transaction Processing](../Datasources/OracleATP.md)
* [Oracle Autonomous JSON Database](../Datasources/OracleAJD.md)
* [Oracle CX Sales and B2B Service](../Datasources/OracleCXB2B.md)
* [Oracle E-Business Suite](../Datasources/EBS.md)
* [Oracle Enterprise Resource Planning ERP](../Datasources/OracleERP.md)
* [Oracle Essbase](../Datasources/OracleEssbase.md)
* [Oracle Human Capital Management](../Datasources/OracleHCM.md)
* [Oracle Product Lifecycle Management](../Datasources/OraclePLM.md)
* [Oracle Sales Cloud](../Datasources/OracleSalesCloud.md)
* [Oracle Service Thin](../Datasources/OracleServiceThin.md)
* [Oracle SID Thin](../Datasources/OracleSidThin.md)
* [Oracle Supply Chain Management](../Datasources/OracleSCM.md)
* [Oracle Taleo](../Datasources/Taleo.md)
* [Pardot](../Datasources/Pardot.md)
* [PeopleSoft](../Datasources/PeopleSoft.md)
* [Pivotal Greenplum](../Datasources/PivotalGreenplum.md)
* [PostgreSQL](../Datasources/Postgres.md)
* [Progress OpenEdge](../Datasources/OpenEdge.md)
* [Quickbooks Desktop](../Datasources/QBDesktop.md)
* [RSS](../Datasources/rss.md)
* [Salesforce](../Datasources/Salesforce.md)
* [Salesforce Marketing Cloud](../Datasources/SFMarkertingCloud.md)
* [SAP Business One](../Datasources/SAPBusinessOne.md)
* [SAP Concur](../Datasources/SAPConcur.md)
* [SAP Hana](../Datasources/SAPHana.md)
* [SAP Netweaver](../Datasources/SAPNetweaver.md)
* [Shopify](../Datasources/Shopify.md)
* [Siebel](../Datasources/Siebel.md)
* [Smartsheets](../Datasources/Smartsheet.md)
* [Snowflake](../Datasources/Snowflake.md)
* [Sugar CRM](../Datasources/SugarCRM.md)
* [Suite CRM](../Datasources/SuiteCRM.md)
* [Sybase](../Datasources/Sybase.md)
* [Teradata](../Datasources/terradata.md)
* [Vertica](../Datasources/Vertica.md)
* [XML](../Datasources/XML.md)

---

[[&#9664; Back to Notifications](../notification.md)] [[Create Warehouse Config &#9654;](../rjwarehouseconfig.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
