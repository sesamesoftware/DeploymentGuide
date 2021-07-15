 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a> <h1 align="center"> Oracle MarketPlace </h1>

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

While the Server is being provisioned

![provisioning](../images/provisioning.png)

* This would to add the ingress rule to the vcn
* You will need to add port 8080 to you ingress rules

![Ingress Rule](../images/addIngressRule.png)

once it is running

![running](../images/computinfo.png)

* copy the public ip address
* in a txt file create a url with the following pattern `http://{ip address}:8080/rj`
  * replace {ip address} with the public ip address


---
 [[marketplace install](installWithMarketPlace.md)] [[Upgrade &#9654;](upgrade.md)]