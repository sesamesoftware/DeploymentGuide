1. Get Login URL from **&#9776; &rarr; Identity & Security &rarr; Federation &rarr; OracleIdenityCloudService &rarr; Oracle Identity Cloud Service Console**
   1. `https://<idcs-url>/ui/v1/adminconsole`
2. Navigate to "Applications" tab
    ![apps tab](../../images/IDCS1.png)
3. Click "Add" button and Choose "Confidential Application"
    ![add](../../images/IDCS2.png)
4. Enter a name e.g.: "Analytics_Token_App", Click Next
   ![name](../../images/IDCS3.png)
5. Click "Configure this application as a client
   1. "Select allowed grant types: "Resource Owner", "Client Credentials" and "JWT Assertion"
   2. In "Allowed Operations", select "On behalf Of"
   3. In "Grant the client access to Identity Cloud Service Admin APIs",
   4. click "Add" and select "Me"
   ![grant](../../images/IDCS4.png)
6. click add agin then next
   ![next](../../images/IDCS5.png)
7. click next
   ![next](../../images/IDCS6.png)
8. Click Finish
   ![next](../../images/IDCS7.png)
9. Copy and save the Client IDand Client SecretStep
     ![next](../../images/IDCS8.png)
10. Activate the applicationStep
    ![next](../../images/IDCS9.png)
11. Generate Access Token
    ![next](../../images/IDCS10.png)
12. Click on Download Token
    ![next](../../images/IDCS11.png)
    * A token file will be generated with name as “tokens.tok”
13. Extract Token from tokens.tok File
    Open tokens.tok file. it will look something like

    ```json
    {"access_token":"eyJ4NXQjUzI1NiI6Imt5bk1iQ ... ... ... 0jxcCw5oR0ajaNw"}
    ```

    extract the value from the Key access_token. This is what you will need to create an OAC instance
