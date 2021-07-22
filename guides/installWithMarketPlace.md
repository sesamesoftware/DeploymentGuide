 <a href="http://www.sesamesoftware.com"><img align=left src="../images/RJOrbit110x110.png"></img></a> <h1 align="center"> Oracle MarketPlace </h1>

[[Installation](installguide.md)] [[Registration](RegistrationGuide.md)] [[Configuration](configurationGuide.md)] [[Datasource](DatasourceGuide.md)]

---

There are two ways to start installing from the market place

* License Type depends on the number of Junctions you will need (MS SQLServer, ADW, CSV, JSON, NetSuite, Salesforce, etc.) Standard is 4 and under, Enterprise is 5 and above.

You can find Relational Junction from the following links:

* [Standard License](https://cloudmarketplace.oracle.com/marketplace/en_US/listing/63628618)
* [Enterprise License](https://cloudmarketplace.oracle.com/marketplace/en_US/listing/84537680)

Or you can also to go thorough the console to the marketplace:
**&#9776; &rarr; Marketplace &rarr; All Applications**

Search for `Relational Junction` and choose the appropriate license type.

![License type](../images/marketplace.png)

This will open up the acceptance dialog in this example we will be using the standard version. 

![Standard license](../images/marketplaceStandard.png)

* Select Compartment you wish the install in
* Accept Terms of usage
* Launce

Once you launch it will bring up the create compute screen.

![Install name](../images/marketplaceinstallname.png)

* Create a meaningful name
* Verify the compartment
* Choose which availability domain you want to use

![shape](../images/marketplaceimageandshape.png)

* Verify image is correct.
* Minimum shape is a 2.4 you can increase this here but most use cases are met in a 2.4 shape.

![networking](../images/marketplaceNetworking.png)

* Choose your VCN
* Choose your Subnet

![ssh](../images/marketplacessh.png)

* You will need to generate and save keys to local system our use existing keys.

![boot volume](../images/marketplaceBootvolumn.png)

* Specify boot volume size min recommendation is 200 gb

Click Create.

---

[[&#9664; Installation](installguide.md)] [[Upgrade &#9654;](upgrade.md)]

<p align="center" >  <a href="http://www.sesamesoftware.com"><img align=center src="../images/poweredBy.png" height="80px"></img></a> </p>
