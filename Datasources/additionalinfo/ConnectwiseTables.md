 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a>

[comment]: # (Change Heading to reflect Datasource)

#  Oracle Service Thin

[comment]: # (Leave Nav BAR untouched)

[[Installation](../guides/installguide.md)] [[Registration](../guides/RegistrationGuide.md)] [[Configuration](../guides/configurationGuide.md)] [[Datasource](../guides/DatasourceGuide.md)]

---

[comment]: # (Leave Or Alter Required info as needed)

### *Available Tables*

Connectwise Datasources can download a specific list of tables. 

### Steps

[comment]: # (step 1 is common to all Datasources)
[comment]: # (Step 2.1and 2.2 should be adjusted for Data Source specific)
[comment]: # (Step 3 should be Image of the datasource you can add the screenshot to the images folder or create a placeholder like {image of datasource screen})
[comment]: # (adjust step 4 and below as needed)

1. In the warehouse config under database design, set objects downloaded to restricted. 
2. list the following tables in the download.config or create a new download.config.connectwise with the following tables:
```
   company/addressFormats
   company/communicationTypes
   company/companies
   company/companies/info/types
   company/companies/statuses
   company/companies/types
   company/companyPickerItems
   company/companyTypeAssociations
   company/configurations
   company/configurations/statuses
   company/configurations/types
   company/contactTypeAssociations
   company/contacts
   company/contacts/departments
   company/contacts/relationships
   company/contacts/types
   company/countries
   company/entityTypes
   company/managedDevicesIntegrations
   company/management
   company/managementItSolutions
   company/marketDescriptions
   company/noteTypes
   company/ownershipTypes
   company/portalConfigurations
   company/portalConfigurations/invoiceSetup/paymentProcessors
   company/portalSecurityLevels
   company/portalSecuritySettings
   company/states
   company/teamRoles
   expense/classifications
   expense/entries
   expense/info/taxTypes
   expense/paymentTypes
   expense/reports
   expense/types
   finance/accounting/batches
   finance/accounting/unpostedexpenses
   finance/accountingPackageSetup
   finance/accountingPackages
   finance/agreements
   finance/agreements/types
   finance/batchSetups
   finance/billingCycles
   finance/billingSetups
   finance/billingStatuses
   finance/billingTerms
   finance/currencies
   finance/deliveryMethods
   finance/glAccounts
   finance/glAccounts/mappedTypes
   finance/glCaptions
   finance/glpaths
   finance/info/currencyCodes
   finance/info/taxIntegrations
   finance/invoiceEmailTemplates
   finance/invoiceTemplateSetups
   finance/invoiceTemplates
   finance/invoices
   finance/taxCodes
   finance/taxIntegrations
   marketing/campaigns/statuses
   marketing/campaigns/subTypes
   marketing/campaigns/types
   marketing/groups
   procurement/adjustments/types
   procurement/catalog
   procurement/categories
   procurement/manufacturers
   procurement/products
   procurement/purchaseorderstatuses
   procurement/settings
   procurement/shipmentmethods
   procurement/subcategories/
   procurement/types
   procurement/unitOfMeasures
   procurement/warehouseBins
   procurement/warehouses
   project/phaseStatuses
   project/projectTypes
   project/projects
   project/securityRoles
   project/statusIndicators
   project/statuses
   project/tickets
   sales/activities
   sales/activities/statuses
   sales/activities/types
   sales/opportunities
   sales/opportunities/ratings
   sales/opportunities/statuses
   sales/opportunities/types
   sales/orders/statuses
   sales/probabilities
   sales/roles
   sales/stages
   schedule/calendars
   schedule/colors
   schedule/details
   schedule/entries
   schedule/holidayLists
   schedule/portalcalendars
   schedule/reminderTimes
   schedule/statuses
   schedule/types
   service/SLAs
   service/boards
   service/codes
   service/emailTemplates
   service/impacts
   service/info/boards
   service/info/boardtypes
   service/locations
   service/priorities
   service/scheduling/members/info
   service/serviceSignoff
   service/severities
   service/sources
   service/teams
   service/templates
   service/ticketLinks
   service/tickets
   system/allowedorigins
   system/apiMembers
   system/authAnvils
   system/connectWiseHostedScreens
   system/connectwisehostedsetups
   system/cwTimeZones
   system/departments
   system/emailExclusions
   system/emailTokens
   system/inOutTypes
   system/info/departmentlocations
   system/info/departments
   system/info/links
   system/info/locales
   system/info/locations
   system/info/members
   system/info/personas
   system/info/standardNotes
   system/integratorlogins
   system/kpiCategories
   system/kpis
   system/links
   system/locations
   system/members
   system/members/types
   system/menuentries
   system/myCompany/corporateStructure
   system/myCompany/corporateStructureLevels
   system/myCompany/crm
   system/myCompany/other
   system/myCompany/timeExpense
   system/mySecurity
   system/mycompany/documents
   system/mycompany/info/services
   system/mycompany/reportingServices
   system/mycompany/services
   system/notificationRecipients
   system/osgradeweights
   system/parsingTypes
   system/parsingVariables
   system/portalReports
   system/securityroles
   system/settings
   system/setupScreens
   system/standardNotes
   system/surveys
   system/timeZoneSetups
   system/todayPageCategories
   system/workflows
   system/workflows/tableTypes
   time/chargeCodes
   time/entries
   time/sheets
   time/timePeriodSetups
   time/workRoles
   time/workTypes
```
[[&#9664; Datasource Guide](../guides/DatasourceGuide.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../../images/poweredBy.png" height="80px"></img></a> </p>
