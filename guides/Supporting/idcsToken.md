Get Login URL from **&#9776; &rarr; Identity & Security &rarr; Federation &rarr; OracleIdentityCloudService &rarr; Oracle Identity Cloud Service Console**

`https://<idcs-url>/ui/v1/adminconsole`

Navigate to "Applications" tab

![apps tab](../../images/IDCS1.png)

 Click "Add" button and Choose "Confidential Application"
![add](../../images/IDCS2.png)
Enter a name e.g.: "Analytics_Token_App", Click Next
![name](../../images/IDCS3.png)
Click "Configure this application as a client

* Select allowed grant types:
  * Resource Owner
  * Client Credentials
  * JWT Assertion
* In "Allowed Operations", select
  * On behalf Of
* In "Grant the client access to Identity Cloud Service Admin APIs"
  * click "Add"
  * select "Me"

![grant](../../images/IDCS4.png)

click add agin then next

![next](../../images/IDCS5.png)

click next

![next](../../images/IDCS6.png)

Click Finish

![next](../../images/IDCS7.png)

Copy and save the Client IDand Client SecretStep

![next](../../images/IDCS8.png)

Activate the applicationStep

![next](../../images/IDCS9.png)

Generate Access Token

![next](../../images/IDCS10.png)

Click on Download Token

![next](../../images/IDCS11.png)

A token file will be generated with name as “tokens.tok”

Extract Token from tokens.tok File

Open tokens.tok file. it will look something like

```json
{"access_token":"eyJ4NXQjUzI1NiI6Imt5bk1iQ ... ... ... 0jxcCw5oR0ajaNw"}
```

extract the value from the Key access_token. This is what you will need to create an OAC instance
