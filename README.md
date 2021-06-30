<img  src="images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="images/RJOrbitLogo-2021Final.png" width="100">

# Deployment Guide 

[![Pre-Installation](images/Button_PreInstall.png)](guides/installguide.md)[![Installation](images/Button_Installation.png)](guides/installguide.md)[![Registration](images/Button_Registration.png)](guides/RegistrationGuide.md)[![Configuration](images/Button_Configuration.png)](guides/configurationGuide.md)[![Datasource](images/Button_Datasource.png)](Datasources/README.md)

---

## Pre-Install

Data Gathering

* Datasource Credentials
  * Target Database [see Datasource Guide for specifics](Datasources/README.md)
  * Source Data [see Datasource Guide for specifics](Datasources/README.md)
* Smtp Information
  * Information needed
    * SMTP Server: ip/named server 
    * Port: port to connect on default is 25
    * mail from : who is the from on the email being sent *(ie rj@sesamesoftware.com)*
    * Username: login for mail server (optional, server dependant rules)
    * Password: password to the server (optional, server dependant rules)
    * Use tls: true/false if server uses TLS
  * Cloud email accounts
    * Gmail 
      * SMTP Server: `smtp.gmail.com`
      * Port: `587`
      * mail from : must be an actual account *(ie rj@sesamesoftware.com)*
      * Username: login for mail server (Required)
      * Password: password to the server (Required)
      * Use tls: `true`
    * office 365
      * SMTP Server: `smtp.office365.com`
      * Port: `587`
      * mail from : must be an actual account *(ie rj@sesamesoftware.com)*
      * Username: login for mail server (Required)
      * Password: password to the server (Required)
      * Use tls: true

[Pre-Installation](guides/installguide.md)