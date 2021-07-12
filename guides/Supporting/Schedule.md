 <a href="http://www.sesamesoftware.com"><img align=left src="../../images/RJOrbit110x110.png"></img></a>

## Relational Junction Scheduler Guide

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

The built-in scheduler on each job allows you to run on an automated schedule without additional setup using a 6 character cron expressions.

![scheduler](../images/rjscheduler.PNG)

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

---
[[&#9664; Job Setup](../JobSetup.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../../images/poweredBy.png" height="80px"></img></a> </p>
