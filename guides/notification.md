 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

# Relational Junction Global Settings

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

These instructions are the set up for Relational Junction email notifications, if desired. This step is optional and can be skipped and set up later.

![notification](../images/ConfigNotification.png)

* SMTP Information
  * Information Required
    * SMTP Server: IP/Named server
    * Port: Port to connect on. Default is 25.
    * Mail from : The from field on the notifcation email being set. *(ie rj@sesamesoftware.com)*
    * Username: Login for mail server (optional, server dependant rules)
    * Password: Password to the server (optional, server dependant rules)
    * Use TLS: True/False if the server uses TLS.
  * Cloud email accounts
    * Gmail
      * SMTP Server: `smtp.gmail.com`
      * Port: `587`
      * Mail from : Must be an actual account *(ie rj@sesamesoftware.com)*
      * Username: Login for mail server (Required)
      * Password: Password to the server (Required)
      * Use TLS: `True`
    * office 365
      * SMTP Server: `smtp.office365.com`
      * Port: `587`
      * Mail from : Must be an actual account *(ie rj@sesamesoftware.com)*
      * Username: Login for mail server (Required)
      * Password: Password to the server (Required)
      * Use TLS: True
  
![ETL Job Default Settings](../images/jobDefaultSetting.png)

* Reject Log level: Error
* Force: Unchecked
* Include Logs: Checked
  * Whether logs are included as an attachement on email.
* Mail To: 
  * A single email address, distribution list or a comma separated list of address that will receive an email when jobs are successful should be at least one address for testing. the Job will determine the rule on when emails are sent.
* Mail Exception To: 
  * A single email address, distribution list or a comma separated list of address that will receive an email when jobs fail should be at least one address. the Job will determine the rule on when emails are sent.
* Log Retention: 7 days

---

[Configuration](guides/configurationGuide.md) | [&#9664; **Notifications** &#9654;](notification.md) | [Datasources](DatasourceGuide.md) | [RJWarehouse Config](rjwarehouseconfig.md) | [Create and Run Job](JobSetup.md)


<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
