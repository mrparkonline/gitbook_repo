# Interacting with Multiple Table

Often a database will contain multiple tables that have relationships. The benefits of storing data in multiple tables is to reduce redundancy through normalization.

Since there are multiple related tables, there needs to be a method to query multiple tables together to output meaningful information.

This is done with the concept of `join`.

## Join Queries in SQL

* _When joining tables, we often think about having a `"left"` table and a `"right"` table._
* _To join two tables, we often try to match the following attributes:_
  * A `primary key` of the left table and a `foreign key` of the right table (which holds the same data as the primary key on the left)
    * This shows that the left and the right table are related by the primary + foreign key relationship
  * The inverse is also true; the left table can contain a foreign key which is the primary key of the right table.
  * Two tables can also be joined by matching an identical attribute with matching fields.

{% hint style="warning" %}
**Tables should not be joined by connecting two non-related attributes.**
{% endhint %}

### Join Queries

```
DB Notes:

left_t -> left table
right_t -> right table

left_t.fk -> left table foreign key
right_t.pk -> right table primary key

fk and pk have identical fields
```

**INNER JOIN**: Returns records that have matching values in both tables. If there is no match, the result set will not include those rows.

```sql
SELECT *
FROM left_t
INNER JOIN right_t ON left_t.fk = right_t.pk;
```

**LEFT JOIN**: Returns all records from the left table, and the matched records from the right table. If there is no match, the result is NULL on the side of the right table.

```sql
SELECT *
FROM left_t
LEFT JOIN right_t ON left_t.fk = right_t.pk;
```

**RIGHT JOIN**: Returns all records from the right table, and the matched records from the left table. If there is no match, the result is NULL on the side of the left table.

```sql
SELECT *
FROM left_t
RIGHT JOIN right_t ON left_t.fk = right_t.pk;
```

**FULL JOIN:** Returns all records when there is a match in either left or right table. If there is no match, the result is NULL on the side where there is no match.

```sql
SELECT *
FROM left_t
FULL OUTER JOIN right_t ON left_t.fk = right_t.pk;
```

{% hint style="success" %}
Using \* will often represent repeating values (especially the matching keys)

Therefore, it is recommended to `SELECT` the only required attributes desired.
{% endhint %}

### Example

Consider the following tables:

```
Orders(OrderID, Item, Quantity, CustomerID)
Customers(CustomerID, CustomerName)
```

Our goal is to display and match the `OrderID` to `CustomerName`

#### Query

```sql
SELECT Orders.OrderID, Customers.CustomerName
FROM Orders
INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
```

* Our select query target two attributes:
  * `Orders.OrderID`
  * `Customers.CustomerName`
    * It is important that we use a period after a table name to target our desired attribute

```sql
FROM Orders INNER JOIN Customers
```

* This clause establishes our left and right clauses

```sql
ON Orders.CustomerID = Customers.CustomerID;
```

* This instructs our join clause where `Orders.CustomerID` matches `Customers.CustomerID`
