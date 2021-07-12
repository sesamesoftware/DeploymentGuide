<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

[comment]: # (Change Heading to reflect Datasource)

## Datasource Guide for Oracle Product Lifecycle Management

[comment]: # (Leave Nav BAR untouched)

[![Pre-Installation](../images/Button_PreInstall.png)](../guides/installguide.md)[![Installation](../images/Button_Installation.png)](../guides/installguide.md)[![Registration](../images/Button_Registration.png)](../guides/RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](../guides/configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](README.md)
---
[comment]: # (Leave Or Alter Required info as needed)

### *Required Information*

* **User**
* **Password**
* **Endpoint**

### Steps

[comment]: # (step 1 is common to all Datasources)
[comment]: # (Step 2.1and 2.2 should be adjusted for Data Source specific)
[comment]: # (Step 3 should be Image of the datasource you can add the screenshot to the images folder or create a placeholder like {image of datasource screen})
[comment]: # (adjust step 4 and below as needed)

1. From the front page of the RJ UI, go to the left hand side and click **Datasources --> New Datasource**

2. On the next screen, choose a label for your Datasource.
	1. Recommended: ‘Source Oracle PLM’ or something similar.
	2. Select OraclePLM Template
	3. Click Save
   
3. ![OraclePLM Datasource](../images/oraclescm.png)

4. Logon Information Section
	1. **User**: *Oracle PLM REST API User*
	2. **Password**: *Password for the given user*
	3. **Endpoint**: *Endpoint to the Oracle PLM REST API such as **https://[SERVER]/fscmRestApi/resources/11.13.18.05/** (please include the last forward slash)*
   
5. Click Test
	1. You see Connection Test Successful
   
6. Extended Properties
	1. **Datetime Formats**: Format of the datetime fields defined in the "Date Fields" property The standard Oracle PLM datetime formats are already pre-populated.
	2. **Date Fields**: The fields in the source objects that are date fields (comma delimited string). You can also use the star (\*) wildcard like such: LastModified\*
	3. **Query String**: Additional URL query parameters (must start with &). For Oracle PLM this is normally to expand the children like such:
		1. &expand=versions
		2. &expand=all
	4. **Primary Keys Mapping**: How to identify the primary keys of the objects. Format is (note the comma delimiter): {objectName}:{fieldName},{objectName2}:{fieldName2}
		1. Examples (All Primary Key Mappings are Case Sensitive):
			1. With Wilcard: *.lines:LineId
			2. One to one: expenses:ExpenseId
	5. **Parent Id Mapping**: How to identify the Parent Id of an expanded child. \*NOTE that if the parent is already mapped in the Primary Keys Mapping this can be skipped.
		In the child object table the Parent Id will be mapped to a column named "PARENTID"
		1. Examples of getting the Invoice Lines children from the Invoice object and then mapping the Parent Id.
			1. **Query String**: &expand=invoices.invoiceLines
			2. **Parent Id Mapping**: invoices.invoiceLines:InvoiceId
	6. **JSONPath**: Path the JSON Array of records. Defaults to "items" as seen in this sample JSON. Most likely will not need to modify.
		![OraclePLM Sample JSON](../images/oraclescmjson.png)
	7. **Page Size**: Number of records to return from each REST request (defaults to 100).
	8. **First Record Date**: When doing date range queries this tells the the Job all records are after this date.

7. Click Save and Close.

[![Previous](../images/Left_Arrow_Previous.png)](README.md)