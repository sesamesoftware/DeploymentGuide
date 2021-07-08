<img  src="../../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../../images/RJOrbitLogo-2021Final.png" width="100">

# Install with Oracle Resource Manager

[![Pre-Installation](../images/Button_PreInstall.png)](../README.md)[![Installation](../images/Button_Installation.png)](installguide.md)[![Registration](../images/Button_Registration.png)](RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](../Datasources/README.md)

---

## Getting Started

First step is to download The ORM compressed file [here](../release/RelationalJunctionOCIStack.zip)

### Creating the Stack

1. login to your oci tenancy
2. click &#9776; &rarr; Developer Services &rarr; Resource Manager &rarr; Stacks
3. ![Resource Manager Stacks](../images/Stacks.png)
   1. Set the compartment you whish to build in
   2. click Create Stack
4. ![Create Stack](../images/CreateStack.png)
   1. select My Configuration
   2. Select .zip File
   3. Browse to the download location of RelationalJunctionOCIStack.zip
   4. click ok
5. You can optionally change the name
6. change compartment to create the stack in
7. and add tags
8. clickNext

### Configuring the Stack Variables

#### The options

![Infrastructure Options](../images/Infrastructure_Options.png)

<details><summary> Relational Junction Configuration</summary>

![Relational Junction Configuration](../images/RelationalJunctionConfiguration.png)

1. verify compartment
2. you can optionally set server name
3. select shape
   1. VM.Standard2.4 *default*
   2. VM.Standard2.8
   3. VM.Standard2.16
   4. VM.Standard2.24
4. you can choose License Type
   1. Relational Junction Standard *default*
   2. Relational Junction Enterprise
   3. Relational Junction BYOL
5. upload you public ssh key
6. you can create one following these [directions](Supporting/OCI-Prerequisites.md##setup-keys)
7. Chose Availability Domain. values are 1-3

</details>

<details><summary>Virtual Cloud Network Configuration Existing</summary>

![Virtual Cloud Network Configuration Existing](../images/VirtualCloudNetworkConfigurationExisting.png)

1. Choose Compartment of existing VCN
2. Select VCN
3. Select Private and Public Subnets

</details>

<details><summary>Virtual Cloud Network Configuration New</summary>

![Virtual Cloud Network Configuration New](../images/VirtualCloudNetworkConfigurationNew1.png)

</details>

<details><summary>Autonomous Database Warehouse Configuration</summary>

![Autonomous Database Warehouse Configuration](../images/AutonomousDatabaseWarehouseConfiguration.png)

</details>

<details><summary>Autonomous Transaction Processing Configuration</summary>

![Autonomous Transaction Processing Configuration](../images/AutonomousTransactionProcessingConfiguration.png)

</details>

<details><summary>Autonomous JSON Database Configuration</summary>

![Autonomous JSON Database Configuration](../images/AutonomousJSONDatabaseConfiguration.png)

</details>

<details><summary>Database Systems Configuration</summary>

![Database Systems Configuration](../images/DatabaseSystemsConfiguration.png)

</details>

<details><summary>Object Storage Configuration</summary>

![Object Storage Configuration](../images/ObjectStorageConfiguration.png)

</details>

<details><summary>Oracle Analytics Cloud Configuration</summary>

![Oracle Analytics Cloud Configuration](../images/OracleAnalyticsCloudConfiguration.png)

</details>

### Reviewing

### upgrading to Latest version
