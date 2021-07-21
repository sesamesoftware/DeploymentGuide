 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

# Warehouse Configuration - Select Tables to Load

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

## Select Tables to Load

Select tables to load is a tool that allows you to create/edit download, upload, and exclude files.


![Select Tables to Load Menu, NetSuite Example](../images/selecttablestoload.png)

#### download.config

Select the RJWarehouse → Select Tables to Load menu, and choose the specific objects or tables you want to load.

1. From the front page of the RJ UI, go to the menu on the left and click Warehouse &rarr; Select Tables to Load
2. Choose the configuration for your download.
3. Chose your object list.
   1. If this is your first time, use ```download.config```. If you have a config file already select it in the dropdown.
4. Click the Refresh Available Objects button, wait until the tables load.
   1. On the left are the available objects in your datasource. On the right are the objects in your download list.
5. Objects can be moved using the center Add/Remove buttons. SHIFT+Click and CTRL+Click can be used.
6. Click Save
7. In the pop-up give your new ```download.config``` a new name, meaningful and/or note the name down.
8. Click Save.

#### exclude.config

The exclude configs are already populated with some standard objects.  Upon initialization, a checkExcludeGlobal will run creating an exclude.config.default file looking at the current Salesforce object list and verifying which objects are usable or not.  This file will reside in the RJ_HOME\1000\rjwarehouse\conf folder.

To add this to your current job:

1. From the menu on the left, go to Warehouse &rarr; Config List
2. Select your config file.
3. Verify you are in Expert Mode (radial button at the top of the config) and then click Database Design.
4. Set Objects Downloaded to Restricted
5.  In the Download Config and Exclude Config fields, enter the ```download.config``` and/or ```exclude.config``` you just built.
6.  Click Save

Note: Even if your configuration file is set to restricted mode you can still download or upload a specific object using one of the single object commands.




---

[[&#9664; Create Datasources](DatasourceGuide.md)] [[create and Run Job &#9654;](JobSetup.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>