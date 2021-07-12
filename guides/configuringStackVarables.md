
<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

# Configuring the Stack Variables

[![Installation](../images/Button_Installation.png)](installguide.md)[![Registration](../images/Button_Registration.png)](RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](DatasourceGuide.md)

---

## The options

![Infrastructure Options](../images/Infrastructure_Options.png)

### Relational Junction Configuration

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

### Virtual Cloud Network Configuration Existing

![Virtual Cloud Network Configuration Existing](../images/VirtualCloudNetworkConfigurationExisting.png)

1. check Use existing VCN
2. Choose Compartment of existing VCN
3. Select VCN
4. Select Private and Public Subnets

#### Virtual Cloud Network Configuration New

![Virtual Cloud Network Configuration New](../images/VirtualCloudNetworkConfigurationNew1.png)

Make any changes to the defaults  such as names and or cider blocks

[[Create Stack](installwithORM.md)] [[Review and Apply](reviewAndApply.md)]
