# Customers and Orders – SQL JOINs Practice

##  Project Overview

This project demonstrates a relational database structure using two tables: `Customers` and `Orders`. The goal is to understand how different SQL JOIN operations behave when merging data from related tables.

Screenshots of the table data and JOIN query results have been included to visually support the explanations.


##  Tables Description

### Customers Table

Stores information about customers.

- `CustomerID`: Unique identifier for each customer.
- `Name`: Name of the customer.
- `City`: City of the customer.

### Orders Table

Stores order transactions made by customers.

- `OrderID`: Unique identifier for each order.
- `CustomerID`: ID of the customer who made the order.
- `Product`: Product name.
- `Amount`: Total amount of the order.

---

##  Table Relationship

The `CustomerID` in the `Orders` table is a foreign key that references the `CustomerID` in the `Customers` table.

- One customer can have multiple orders.
- Each order is placed by one customer.
- This establishes a **one-to-many** relationship.

---

##  JOIN Operations

### INNER JOIN

- Returns only the records with matches in both tables.
- Used to find customers who have placed orders.

### LEFT JOIN

- Returns all customers.
- Includes their order details if they have any.
- If not, order fields will be `NULL`.

### RIGHT JOIN

- Returns all orders.
- Includes the customer who placed each order.
- If the order is not linked to any customer, customer fields will be `NULL`.

### FULL OUTER JOIN

- Combines LEFT and RIGHT JOIN results.
- Returns all customers and all orders.
- Unmatched data from either side appears with `NULL` values.

---

##  Sample Data Notes

- Some customers have multiple orders.
- Some orders have no matching customer (`CustomerID` doesn't exist).
- Some customers have no orders.

Screenshots are included to illustrate these cases for each JOIN type.

---

##  Learning Goals

By completing this project, you will:

- Understand relational database design.
- Practice SQL JOINs with real-world structure.
- Know how and when to use INNER, LEFT, RIGHT, and FULL JOINs.
- Visually interpret results using the included screenshots.
