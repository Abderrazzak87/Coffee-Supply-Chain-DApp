# Coffee Supply Chain

## Description
Ethereum DApp that demonstrates a Supply Chain flow between a Seller and Buyer. The user story is similar to any commonly used supply chain process. A Seller can add items to the inventory system stored in the blockchain. A Buyer can purchase such items from the inventory system. Additionally a Seller can mark an item as Shipped, and similarly a Buyer can mark an item as Received.

### Actors
* Farmer
* Distributor
* Retailer
* Consumer

### Actions
* **Farmer** – A Farmer can harvest coffee, process coffee, pack coffee, add coffee to sell, ship coffee
* **Distributor** – A Distributor can buy coffee
* **Retailer** – A Retailer can receive coffee
* **Consumer** – A Consumer can purchase coffee

Different steps that a product (coffee)  goes through until it will be bought by a consumer like showed in the UML Activity Digram below.

## UML Diagrams

### Activity Diagram
![Activity Diagram](./uml/SupplyChainDAppActivityDiagram.jpeg "Activity Diagram")

### Sequence Diagram
![Sequence Diagram](./uml/SupplyChainDappSequenceDiagram.jpeg "Sequence Diagram")

### State Diagram
![State Diagram](./uml/SupplyChainDAppStateDiagram.jpg "State Diagram")

### Data Model Diagram
![Data Model Diagram](./uml/SupplyChainDAppClassDiagram.jpeg "Data Model Diagram")

## User Interface

### Role Management Section
User can can add a new farmer, distributor, retailer or a consumer to the list of users of the DApp.

![Role Management Section](./images/ftc_role_management.png "Role Management Section")

### Product Overview Section
User can fetch information about concrete product.
* **Fetch Data 1** – Fetch farmer related data
* **Fetch Data 2** – Fetch the product data related the distributor, the retailer and the consumer.
* **Fetch Image** – Fetch the product image stored in the INFURA IPFS node.

![Product Overview](./images/ftc_product_overview.png "Product Overview")

### Farmer Details Section
This form is used to show the Farmer ID, Name, coordinates (Long and Lat) fetched by the **Fetch Data 1** button.
It is used also to input the farmer's information.
In this section a Farmer can harvest coffee → process coffee → pack coffee bags → prepare them for sale.
* **Harvest** – This button calls the harvestItem() method of the SupplyChain.sol contract.
* **Process** – This button calls the processItem() method of the SupplyChain.sol contract.
* **Pack** – This button calls the packItem() method of the SupplyChain.sol contract.
* **Buy** – This button calls the buyItem() method of the SupplyChain.sol contract.

![Farmer Details](./images/ftc_farm_details.png "Farm Details")

### Product Details Section
This form is used to show the information fetched by the **Fetch Data 2** button.
It is used also to input the product's information.
In this section a distributor can buy Coffee and a farmer can ship Coffee to Retailer.
Retailer can receive coffee. And finally Consumer can purchase Coffee from Retailer.
* **Buy** – This button calls the buyItem() method of the SupplyChain.sol contract.
* **Ship** – This button calls the shipItem() method of the SupplyChain.sol contract.
* **Receive** – This button calls the receiveItem() method of the SupplyChain.sol contract.
* **Purchase** – This button calls the purchaseItem() method of the SupplyChain.sol contract.

![Product Details](./images/ftc_product_details.png "Product Details")

### Transaction History Section
This section contains transaction hashs of all transactions that was produced by processing a product in the supply chain.

![Transaction History](./images/ftc_transaction_history.png "Transaction History")

### IPFS Image Uploader
This section allows to a product owner to upload an image of the product.

![IPFS Image Uploader](./images/ftc_ipfs_image_uploader.png "IPFS Image Uploader")
