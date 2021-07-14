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

* [NetSuite](../Datasources/netsuite.md)
* [Oracle Service Thin](../Datasources/OracleServiceThin.md)
* [Oracle Sid Thin](../Datasources/OracleSidThin.md)
* [Oracle Autonomous Data Warehouse](../Datasources/OracleADW.md)
* [Oracle Autonomous Transaction Processing](../Datasources/OracleATP.md)
* [Oracle Autonomous JSON Database](../Datasources/OracleAJD.md)
* [MySql](../Datasources/MySQL.md)
* [Microsoft Sql Server](../Datasources/MySQL.md)
* [Marketo](../Datasources/Marketo.md)
* [MS Dynamics CRM](../Datasources/MSDynamicsCRM.md)
* [Oracle CX Sales and B2B Service](../Datasources/OracleCXB2B.md)
* [Oracle ERP](../Datasources/OracleERP.md)
* [Oracle Essbase](../Datasources/OracleEssbase.md)
* [Oracle Human Resources Cloud](../Datasources/OracleHCM.md)
* [Oracle Product Lifecycle Management](../Datasources/OraclePLM.md)
* [Oracle Sales Cloud](../Datasources/OracleSalesCloud.md)
* [Oracle Supply Chain Management](../Datasources/OracleSCM.md)

---

[[&#9664; Configure Notification](notification.md)] [[Create Warehouse Config &#9654;](rjwarehouseconfig.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
