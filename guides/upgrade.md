<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

# upgrading to Latest version

[![Installation](../images/Button_Installation.png)](installguide.md)[![Registration](../images/Button_Registration.png)](RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](DatasourceGuide.md)

---

Open command line terminal and run the following:

```ssh -i {path to privatekey} opc@{ip address from RJ_URL} upgrade```

This will bring you  install up to the latest available GA code for example

```bash
ssh -i ~/.ssh/oci opc@129.213.26.247 upgrade
```

once this is complete open a browser tab and navigate to the URL provided in the RJ_URL output.

[[Review and Apply](reviewAndApply.md)] [registration](RegistrationGuide.md)