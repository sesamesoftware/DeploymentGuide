<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

## Relational Junction Global Settings

[![Installation](../images/Button_Installation.png)](installguide.md)[![Registration](../images/Button_Registration.png)](RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](DatasourceGuide.md)

---

Use these instructions to set up email notifications if desired. This Step is optional so can be skipped and done later

![notification](../images/ConfigNotification.png)

* SMTP Information
  * Information needed
    * SMTP Server: ip/named server
    * Port: Port to connect on default is 25
    * Mail from : Who is the from on the email being sent *(ie rj@sesamesoftware.com)*
    * Username: Login for mail server (optional, server dependant rules)
    * Password: Password to the server (optional, server dependant rules)
    * Use TLS: True/False if server uses TLS
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
* Force: unchecked
* include Logs: checked
* Mail To: a single email address, distribution list or a comma separated list of address that will receive an email when jobs are successful should be at least one address for testing. the Job will determine the rule on when emails are sent.
* Mail Exception To: a single email address, distribution list or a comma separated list of address that will receive an email when jobs fail should be at least one address. the Job will determine the rule on when emails are sent.
* Log Retention: 7 days

[[Configuration](guides/configurationGuide.md)] [[Create Datasources](DatasourceGuide.md)]