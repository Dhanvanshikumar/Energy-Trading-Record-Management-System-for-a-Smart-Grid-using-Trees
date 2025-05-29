# Energy-Trading-Record-Management-System-for-a-Smart-Grid-using-Trees (Using B+ Trees)
The goal is to develop a software program that manages energy trading transactions in a smart
grid environment using B+ Trees. Energy trading transactions occur when
energy producers (sellers) sell energy to consumers (buyers) at specified rates. These
transactions need to be accurately recorded, tracked, and analyzed to optimize energy trading
operations, manage financial records, and enable efficient trading management within the grid.

Each transaction is represented as a node in the tree and contains the following attributes:
- Transaction ID: Unique identifier for each transaction.
- Buyer ID: Unique ID of the entity buying energy.
- Seller ID: Unique ID of the entity selling energy.
- Amount of Energy (kWh): The amount of energy traded in kilowatt-hours.
- Price per kWh: The rate applied for this transaction, determined by the seller’s pricing
structure.
- Total Price: Computed as Amount of Energy * Price per kWh.
- Timestamp: Date and time when the transaction occurred.
  
Each seller is stored in a separate tree to allow quick lookups and sorting.
- Seller ID
- Energy rate per kWh below 300 kWh
- Energy rate per kWh above 300 kWh
- List of Regular Buyers: Maintained as a List (Buyers with more than 5 transactions).
- Transaction Subtree: A reference to a tree containing all transactions associated with this
seller.

Each buyer is also stored in a separate tree:
- Buyer ID
- Total Energy Purchased: Sum of all energy bought.
- Transaction Subtree: A reference to a tree containing all transactions associated with this
buyer.

Operations :
1. Add New Transactions
2. Display All Transactions
3. Create a set of Transactions for Every Seller
4. Create a set of Transactions for Every Buyer
5. Find all transactions in a Given Time Period
6. Calculate Total Revenue by Seller
7. Find and Display (in ascending order) the transactions with the Energy Amounts between
certain range.
8. Sort the set of Buyers Based on Energy Bought
9. Sort Seller/Buyer Pairs by Number of Transactions
