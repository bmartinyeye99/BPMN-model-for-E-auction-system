# BPMN-model-for-E-auction-system

## Technologies used:
  -  Camunda modeler
  -  Petri-net
  -  Netgrif-Next-Builder
  -  Java 11
  -  InteliJ
  -  JavaFX

## Project Scope
Auction systems are an essential part of electronic marketplaces as they enable users to buy and sell items from anywhere. Sellers can list auctions for their items, and interested bidders with the highest bid get the opportunity to purchase the product in the auction.

The auction begins at a specified time set by the seller. When the seller adds a product and sets the auction date and time, the auction is recorded. At the same time, the seller sets the starting price that potential buyers must exceed to bid on the offered item. During the auction, potential buyers can express their interest in the item by increasing their bids. Users will also have the ability to search for available auctions based on their preferences (e.g., by product or date). E-auctions are evaluated immediately, and participants are informed of the auction result as soon as it ends. Subsequently, the auction winner pays for the item through the system, and the seller ships it.

## Process Descriptions

### PROCESS 1: Placing a Bid

**Description:** If a buyer decides to place a bid on an item listed in an auction, they first browse the auction listings. They select the item they want to bid on and enter their bid amount. They are then presented with new information about the product and confirm their bid. The system checks if the entered bid is higher than the previous bid and updates the item with the new highest bid if it is. The user is notified of a successful bid. If the buyer enters a lower amount, the item is not updated, and the buyer is prompted to enter a valid (higher) amount.

**Input tokens:** amount, item  
**Output tokens:** placed bid  
**Transitions:** item selection, bid entry, bid confirmation, item update  
**States:** bid entered, bid confirmed, item updated

### PROCESS 2: Searching for Products in Auction

**Description:** If a user wants to search for a specific product in an auction or filter auctions based on certain criteria, they access the section with the auction product listings. They can set filters or leave them at default settings to view available products based on the applied filters. The user selects a product they are interested in, and the system displays detailed information about the selected product.

**Input tokens:** filter, product  
**Output tokens:** (specific) product  
**Transitions:** product selection, filter entry, filter confirmation, display available products, display specific product  
**States:** filter entered, filter confirmed, specific product displayed

### PROCESS 3: Adding an Item to Auction

**Description:** The process of adding an item to an auction begins when a seller chooses the option to create an auction. They then fill in all the basic auction details, such as date, start time, duration, initial price, and the item being offered. If the entered details are correct, the seller confirms them and is redirected to fill in the details about the offered item. During this step, the seller adds photos and a description of the item. They can confirm or edit these details and add them again. After confirming the accuracy of the details, the system presents a summary of all the entered information. The seller can review all the entered details. If any details are incorrect, the system guides the seller to fill in the basic details again, restarting the process. However, if the details are correct, the system records the auction and initiates it at the designated time.

**Input tokens:** option to create an auction, basic details, offered item  
**Output tokens:** offered item  
**Transitions:** record the auction, fill in details, display summary  
**States:** auction recorded, item added, required basic details filled

In the project, we achieved our goal, which was to design a system for electronic auctions for small, standardized purchases of goods and services. We utilized knowledge from practical exercises and lectures. Initially, we described the processes that our system should fulfill. Then, we created a clear process model consisting of these described processes. We defined process roles and assigned them to specific activities within the processes. We also documented these activities in a table.

Based on the process descriptions, we designed their models using Petri nets. We made several changes to the Petri net models during testing, as we discovered simpler solutions and corrected any issues that arose. None of our transitions are L0 live. For one of the processes, we also constructed a reachability graph. Additionally, we designed BPMN models for all processes.
