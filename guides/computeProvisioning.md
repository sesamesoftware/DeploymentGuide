 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a> <h1 align="center"> Oracle MarketPlace </h1>

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

While the Server is being provisioned:

![provisioning](../images/provisioning.png)

* This would to add the ingress rule to the VCN.
* You will need to add port 8080 to your ingress rules.

![Ingress Rule](../images/addIngressRule.png)



Once it is running:

![running](../images/computinfo.png)

* Copy the public IP address from your instance.
* In a text file, create a URL with the following pattern ```http://{ip address}:8080/rj```
  * Replace {IP address} with the public IP address.


---
 [[marketplace install](installWithMarketPlace.md)] [[Upgrade &#9654;](upgrade.md)]
