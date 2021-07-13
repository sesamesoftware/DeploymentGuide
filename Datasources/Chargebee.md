<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

[comment]: # (Change Heading to reflect Datasource)

## Chargebee

[comment]: # (Leave Nav BAR untouched)

[[Installation](../guides/installguide.md)] [[Registration](../guides/RegistrationGuide.md)] [[Configuration](../guides/configurationGuide.md)] [[Datasource](../guides/DatasourceGuide.md)]

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
	1. Recommended: ‘Source Chargebee’ or something similar.
	2. Select Chargebee Template
	3. Click Save
   
3. ![Chargebee Datasource](../images/Chargebee.png)

4. Logon Information Section
	1. **User**: *Chargebee API User*
	2. **Password**: *Password for the given user*
	3. **Endpoint**: *Endpoint to the Chargebee REST API such as **https://[YOURCOMPANY].chargebee.com/api/v2/** (please include the last forward slash)*
   
5. Click Test
	1. You see Connection Test Successful
   
6. Extended Properties
	1. **JSONPath**: Will always default to "list" for Chargebee. No need to set manually.
	2. **Page Size**: Number of records to return from each REST request (defaults to 100).
	3. **First Record Date**: When doing date range queries this tells the the Job all records are after this date.
	4. **Date Fields**: The fields in the source objects that are date fields (comma delimited string). You can also use the star (\*) wildcard like such: LastModified\*
	5. **Datetime Formats**: Dates in Chargebee are stored as 10 digit timestamp to the second (LONG_10). You should not need to modify this setting.
	6. **Query Date Fields**: The date field to do incremental date range queries against. Defaults to updated_at.
	7. **Primary Keys Mapping**: How to identify the primary keys of the objects. Format is (note the comma delimiter): {objectName}:{fieldName},{objectName2}:{fieldName2}
		1. Examples (All Primary Key Mappings are Case Sensitive):
			1. With Wilcard: *.id
			2. One to one: subscriptions:id
	5. **Parent Id Mapping**: This property can be ignored for Chargebee.

7. Click Save and Close.

---

[[&#9664; Datasource Guide](../guides/DatasourceGuide.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
