 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

# Relational Junction install Guide

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

## Pre-Install

Data Gathering

* Datasource Credentials
  * Target Database [see Datasource Guide for specifics](../Datasources/README.md)
  * Source Data [see Datasource Guide for specifics](../Datasources/README.md)
* SMTP Information
  * Information needed
    * SMTP Server: ip/named server
    * Port: Port to connect on default is 25
    * Mail from : Who is the from on the email being sent *(ie rj@sesamesoftware.com)*
    * Username: Login for mail server (optional, server dependant rules)
    * Password: Password to the server (optional, server dependant rules)
    * Use TLS: True/False if server uses TLS

## Install

* The install using Market Place [click here](installWithMarketPlace.md)
  * *Use this for established Tenancy and an rj only install*
* The install using Oracle Resource Manager [click here](installwithORM.md)
  * *Use this for install in most cases, has the ability to spin up the necessary infrastructure*
    * *create or use existing VCN*
    * *Create Rj server*
    * *Create ADB servers*
    * *Create OAC instance*
    * *Create Object Storage Bucket*
* The install using Terraform guide [click here](installwithTerraform.md)
  * *Use this to further customize the ORM package*

---

[[&#9664; Main Menu](../README.md)] [[Registration &#9654;](RegistrationGuide.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
