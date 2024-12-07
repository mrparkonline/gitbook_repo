# Sum & Average Queries

Both the sum and average queries can help us summarize and analyze numerical data in a table.

## Total Sum

The `SUM()` function returns the total sum of a numeric column.

It is useful when calculating how many records from an attribute fits your given condition.

### `SUM()` Query Format

```sql
SELECT SUM(column_name) FROM table_name WHERE condition;
```

## Average of an Attribute

The `AVG()` function returns the average value of a numeric column.

### `AVG()` Query Format

```sql
SELECT AVG(column_name) FROM table_name WHERE condition;
```

## Use Cases for `SUM()` and `AVG()`

Let us assume that we have the following table:

`Products(ProductID, Name, Price, Sold)`

* The sum query can be used to output number of products sold so far in the table

```sql
SELECT SUM(Sold) FROM Products;
```

* The average query can be used to output the average price of all items in the table

```sql
SELECT AVG(Price) FROM Products;
```
