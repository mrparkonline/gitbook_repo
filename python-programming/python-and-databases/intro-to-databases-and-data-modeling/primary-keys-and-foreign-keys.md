# Primary Keys and Foreign Keys

## Primary Key

A **primary key** is a unique identifier for each record in a database table.&#x20;

* It ensures that each record can be uniquely identified and retrieved.&#x20;
* A primary key must contain `unique` values and cannot contain `NULL` values.&#x20;
* Each table can have only one primary key, which can consist of a single column or multiple columns (composite key).

**Example:** In a `Customers` table, the `CustomerID` column can be the primary key:

`Customers` Table

| CustomerID | CustomerName | CustomerAddress |
| ---------- | ------------ | --------------- |
| 1          | John Doe     | 123 Elm St      |
| 2          | Jane Smith   | 456 Oak St      |

### Primary Key's Purpose

* **Uniqueness**: Ensures each record in the table is unique.
* **Indexing**: Often used to create an index, which improves the speed of data retrieval operations.
* **Data Integrity**: Prevents duplicate records and ensures that each record can be uniquely identified.

### Composite Primary Key

A composite primary key is a primary key that consists of two or more columns in a table.&#x20;

This type of key is used when a single column is not sufficient to uniquely identify each row in the table.&#x20;

Instead, the combination of the values in these columns must be unique for each row.

#### When to Use Composite Primary Keys

Composite primary keys are typically used in situations where:

* The table represents a many-to-many relationship between two entities.
* No single column can uniquely identify a row, but a combination of columns can.

## Foreign Key

A **foreign key** is a column or a set of columns in one table that uniquely identifies a row of another table.&#x20;

* The foreign key establishes a relationship between the two tables.&#x20;
* It ensures that the value in the foreign key column matches a value in the primary key column of the referenced table, maintaining referential integrity.

**Example:** In an `Orders` table, the `CustomerID` column can be a foreign key that references the `CustomerID` column in the `Customers` table:

`Orders` Table

| OrderID | CustomerID | ProductID | Quantity |
| ------- | ---------- | --------- | -------- |
| 1       | 1          | 101       | 5        |
| 2       | 2          | 102       | 3        |
| 3       | 1          | 103       | 2        |

### Foreign Key's Purpose

* **Relationships**: Establishes and enforces relationships between tables.
* **Referential Integrity**: Ensures that the value in the foreign key column matches a value in the primary key column of the referenced table, maintaining consistency across the database.

## Referential Integrity

**Referential integrity** is a property of data stating that all its references are valid.&#x20;

In relational databases, it ensures that relationships between tables remain consistent.&#x20;

For example, if a record in the `Orders` table references a `CustomerID` in the `Customers` table, referential integrity ensures that the `CustomerID` exists in the `Customers` table.

* **Prevents Orphan Records**: Ensures that a foreign key value always points to an existing record in the referenced table.
* **Cascading Actions**: Supports cascading updates and deletes. For example, if a customer is deleted, all related orders can also be deleted automatically.
* **Consistency**: Maintains the logical consistency of the database by ensuring that relationships between tables are preserved.
