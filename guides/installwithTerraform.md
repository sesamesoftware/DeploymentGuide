 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

# Install with Terraform

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

## Pre-Requisites

* Install : ```git```
* Install : ```SSH Client```
* Install : [Terraform 0.12.16+](Supporting/OCI-Prerequisites.md#Install-Terraform)

#### Provisioning Using git Repository

1. Clone the Repository:

```bash
git clone https://github.com/sesamesoftware/Terraform-OCI-RelationalJunction.git RelationalJunction

cd RelationalJunction
cp terraform.tfvars.example terraform.tfvars
```

2. Mandatory parameters: env-vars file

|parameter|description|example|
|---|---|---|
|tenancy_ocid|The OCIDof the tenancy found int the console
|user_ocid|
|fingerprint|
|private_key_path|
|compartment_ocid|
|ssh_public_key_path|
|ssh_private_key_path|

Set Values in terraform.tfvars

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

* This first ```init``` gets the source Module from Github:

    ```hcl
    terraform get -update
    ```

* This ```init``` initializes the modules:
  
    ```hcl
    terraform init
    ```

* Check that everything is there:

    ```hcl
    terraform plan
    ```

* Builds the infrastructure:

    ```hcl
    terraform apply
    ```

---

[[&#9664; Installation](installguide.md)] [[Upgrade &#9654;](upgrade.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
