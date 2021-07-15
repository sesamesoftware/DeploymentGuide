<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

[![Pre-Installation](../images/Button_PreInstall.png)](guides/installguide.md)[![Installation](../images/Button_Installation.png)](guides/installguide.md)[![Registration](../images/Button_Registration.png)](guides/RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](guides/configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](README.md)

## Table Selection for ServiceNow

1. From the front page of the RJ UI, go to the left hand side and click **Warehouse --> SELECT TABLES TO LOAD**
2. Select the Warehouse Configuration setup for your ServiceNow Datasource or select any other Configuration to setup the Warehouse Configuration later.
3. Leave the Object List set to -- Select --
4. For each table to be used, enter the API name of the table as presented in ServiceNow into the input box at the bottom of the Selected Objects section and then click the ADD OBJECT button.
5. When all tables have been added click the SAVE button.
   1. A Save modal window will open.
   2. Type the name download.config.servicenow in to the Save as: text field. You will need to use this name in the Warehouse Configuration's Database Design section --> Download Config field.
   3. Click the Save button.
