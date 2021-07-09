<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

## Relational Junction Datasource Guide

[![Installation](../images/Button_Installation.png)](../guides/installguide.md)[![Registration](../images/Button_Registration.png)](../guides/RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](../guides/configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](README.md)

---

## RJ Warehouse Oracle Datasource Setup

1. From the front page of the RJ UI, go to the menu on the left and click **Datasources &rarr; New Datasource**
2. On the next screen, choose a label for your Datasource.
   1. *Recommendation: it should be meaningful like ‘Oracle Target for Netsuite’ or 'Source Netsuite'. Setting your naming Convention from the start will save time in the future and making it quick and easy to find elements later*
3. Select Template for the Technology you are connecting too
4. Click Save

*Use [Datasource Guide](#supported-datasources) for specific guides to datasource templates*

Repeat above for source and target. If you are using Columnar based systems like Snowflake, Redshift as your target we recommend having a metadata datasource for the transactional tables our product creates. This would need to be a row based system but can be a small database like mySQL or SQL express.

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

[Configuration Guide](configurationGuide.md)
