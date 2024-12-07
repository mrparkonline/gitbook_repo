# Counting Rows

The `COUNT()` function in SQL is used to return the number of rows that match a specified condition.

## Use Case #1: Count the number of rows in a table

```sql
SELECT COUNT(*) FROM table_name;
```

We are running the `COUNT()` function on all our attributes from a given table. This will count the number of rows.

We can also just target specific column by providing a `column_name` instead of `*`

```sql
SELECT COUNT(col_name) FROM table_name;
```

## Use Case #2: Counting the number of records that match a condition

A more useful use of counting would be to see how many rows will match a certain condition

```sql
SELECT COUNT(*) FROM table_name WHERE condition;
```

By using the `WHERE` clause with `COUNT`, we can select more meaningful data when required.

## Use Case #3: Counting the distinct values that populates an attribute

In a scenario where an attribute can have repeating values per records (_example: product type sold),_ it is beneficial to count the number distinct values within that attribute

```sql
SELECT COUNT(DISTINCT column_name) FROM table_name;
```

In the SQL query above, we are using the `DISTINCT` keyword to not counting repeating values
