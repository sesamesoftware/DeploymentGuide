 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

# Relational Junction install Guide

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

## Pre-Install

Data Gathering

* Datasource Credentials
  * Target Database [see Datasource Guide for specifics](DatasourceGuide.md)
  * Source Data [see Datasource Guide for specifics](DatasourceGuide.md)
* SMTP Information
  * Information needed
    * SMTP Server: IP or Named server
    * Port: Port to connect on; default 25
    * Mail from : Who the from on the email being sent i.e.; ```rj@sesamesoftware.com```.
    * Username: Login for mail server (Optional, server dependant rules)
    * Password: Password to the server (Optional, server dependant rules)
    * Use TLS: True/False if server uses TLS

## Install

* Install using Market Place, [Click Here](installWithMarketPlace.md).
  * Use this for established Tenancy and an RJ-Only install.
* Install using Oracle Resource Manager, [Click Here](installwithORM.md).
  * Use this for install in most cases, has the ability to spin up the necessary infrastructure.
    * Create or use existing VCN
    * Create RJ Server
    * Create ADB Servers
    * Create OAC instance
    * Create Object Storage Bucket
* Install using the Terraform guide, [Click Here](installwithTerraform.md).
  * Use this to further customize the ORM package

---

[[&#9664; Main Menu](../README.md)] [[Registration &#9654;](RegistrationGuide.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
