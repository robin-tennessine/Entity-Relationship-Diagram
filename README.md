# Entity-Relationship Diagram

After confirming with the client, the possible entities and their attributes, identifiers are:

- **Stocks**: *stock#, companyName, exchangeMarket, description
- **Customers**: *customerID, name, phone, email, address 
- **Portfolio**: customerName, currentValue
- **Logs**: *stock#, *date, openPrice, closePrice
- **Transactions**: *TransactionID, customerID, Portfolio, stock#, quantity, price, date, time

