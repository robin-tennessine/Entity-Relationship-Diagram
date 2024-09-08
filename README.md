# Entity-Relationship Diagrams (ERD)

## Introduction

An Entity-Relationship Diagram (ERD) is a visual representation of the entities within a system and the relationships between them. ERDs are crucial for database design as they help in structuring and organizing data efficiently. They illustrate how entities such as tables or objects relate to one another, which aids in the creation of a database schema that supports the business requirements.

## Method Used: Crow's Foot Notation

In these ERDs, Crow's Foot notation is employed to represent the relationships between entities. Crow's Foot notation, also known as IE (Information Engineering) notation, is a popular method for depicting cardinalities and relationships in a database schema. It uses symbols such as lines and crow's feet to indicate the type and cardinality of relationships between entities.

### Key Symbols in Crow's Foot Notation:
- **Crow's Foot**: Represents "many" in a relationship.
- **Line**: Represents a connection between entities.
- **Circle**: Indicates optionality (zero or one).
- **Straight Line**: Indicates a mandatory relationship (one or more).

## Entity-Relationship Diagram TrueTrade

![ERD Practices - TrueTrade](https://github.com/user-attachments/assets/f188b8e7-2bb5-41ae-98c0-4187137ad078)

After confirming with the client, the possible entities and their attributes, identifiers are:

- **Stocks**: `stock#`, `companyName`, `exchangeMarket`, `description`
- **Customers**: `customerID`, `name`, `phone`, `email`, `address`
- **Portfolio**: `customerName`, `currentValue`
- **Logs**: `stock#`, `date`, `openPrice`, `closePrice`
- **Transactions**: `TransactionID`, `customerID`, `Portfolio`, `stock#`, `quantity`, `price`, `date`, `time`

### Relationships

- A customer must have one or more portfolios (1 or N), and a portfolio must belong to one and only one customer (1 or 1).
- A portfolio may have one or more stocks (0 or N), and a stock may belong to one or more portfolios (0 or N).
- A stock must have one or more logs (1 or N), and one log must belong to one and only one stock (1 or 1).
- A customer may have one or more transactions (0 or N), and each transaction must be done by one and only one customer (1 or 1).
- A portfolio may be in one or more transactions (0 or N), and each transaction must include one and only one portfolio (1 or 1).
- A transaction must have a stock (1 or 1), and a stock may be in one or more transactions (0 or N).

## Entity-Relationship Diagram PizzaHot

![ERD Practices - PizzaHot 2](https://github.com/user-attachments/assets/0360fda9-8c40-42c1-a53d-d916d44c3b31)

This ERD represents the relationships between the entities: **Stores**, **Employees**, **Vendors**, and **Products**.

- **Stores**: `StoreID`, `StoreName`, `Location`, `Contact`
- **Employees**: `EmployeeID`, `SSN`, `Name`, `Gender`, `DoB`, `Position`, `Salary`, `AffiliateStore`, `SupervisedBy`
- **Vendors**: `VendorName`, `Address`, `ContactPerson`
- **Products**: `Name`, `Price`, `Quantity`, `Description`, `VendorName`

### Relationships

- A store may have many employees (0 or N); and one employee must work for one store (1 or 1).
- A store may sell many products (0 or N), and each product can be sold at many stores (0 or N).
- A product must belong to one and only one vendor (1 or 1); and a vendor may provide one or more products (0 or N).
- An employee must be supervised by another employee (1 or 1); and an employee may supervise many other employees (0 or N).
