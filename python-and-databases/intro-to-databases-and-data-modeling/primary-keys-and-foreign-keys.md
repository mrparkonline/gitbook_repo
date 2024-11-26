# Primary Keys and Foreign Keys

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

### Key Concepts





