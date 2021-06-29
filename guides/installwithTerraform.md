<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

# Install with Terraform

[![Pre-Installation](../images/Button_PreInstall.png)](../README.md)[![Installation](../images/Button_Installation.png)](installguide.md)[![Registration](../images/Button_Registration.png)](RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](../Datasources/README.md)

---

##Pre-requisites
* git is installed
* ssh client is installed
* [Terraform 0.12.16+ is installed](Supporting/OCI-Prerequisites.md)

Provisioning using this git repo

Clone the repo:
```bash
git clone https://github.com/sesamesoftware/Terraform-OCI-RelationalJunction.git RelationalJunction

cd RelationalJunction
cp terraform.tfvars.example terraform.tfvars
```

Set Values in terraform.tfvars

Mandatory parameters:

|parameter|description|example|
|---|---|---|
|tenancy_ocid|The OCIDof the tenancy found int the console
|user_ocid|
|fingerprint|
|private_key_path|
|compartment_ocid|
|ssh_public_key_path|
|ssh_private_key_path|

Override other parameters:

|switch|description|Default value|
|---|---|---|
|adw_enabled|Create ADW instance|true|
|atp_enabled|Create ATP instance|true|
|ajd_enabled|Create AJD instance|false|
|rj_enabled|Create Relational Junction instance|true|
|oac_enabled|Create OAC instance|false|
|dbas_enabled|Create DBAS instance|false|
|obs_enabled|Create OBJECT Storage instance|false|
|vcn_use_existing|use an already created VCN|false|



vcn_existing
subnet_public_existing
subnet_private_existing
* Optional parameters to override:

Run Terraform:

```hcl
terraform init
terraform plan
terraform apply
```
