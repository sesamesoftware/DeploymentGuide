<img  src="../images/SesameSoftwareLogo-2020Final.png" width="100"><img align=right src="../images/RJOrbitLogo-2021Final.png" width="100">

## Relational Junction Scheduler Guide

[![Pre-Installation](../images/Button_PreInstall.png)](guides/installguide.md)[![Installation](../images/Button_Installation.png)](guides/installguide.md)[![Registration](../images/Button_Registration.png)](guides/RegistrationGuide.md)[![Configuration](../images/Button_Configuration.png)](guides/configurationGuide.md)[![Datasource](../images/Button_Datasource.png)](Datasources/README.md)

---

The built-in scheduler on each job allows you to run on an automated schedule without additional setup using a 6 character cron expressions.

<img  src="../images/rjscheduler.PNG" height='80' width="800">

The time values increase from left to right in the following order: Seconds, Minutes, Hours, Days, Months, Years.

*/ will repeat on the interval of the numeric value. 

`* */15 * * * *` would repeat a job every 15 minutes.
`* * */2 * * *` would repeat a job every 2 hours.

Jobs can also be scheduled to run in specific intervals by including a comma-separated range.

`* * * 7,14,21,28 * *` would run the 7th, 14th,21st, and 28th days of the month

Or by setting a hyphenated range.

`* * 9-17 * * *` would run a job from 9 am to 5 pm

Other examples:
To schedule a job that runs on the first second, of the first minute, every 2 hours, every day, of every month, every year the expression is: `1 1 */2 * * *`

Useful Website for generating expressions (add a * for the first character, then input the generated expression):
https://crontab.guru/
