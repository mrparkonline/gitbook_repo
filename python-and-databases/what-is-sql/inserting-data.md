# Inserting Data

**CRUD** is a database principle that is crucial for interacting with databases.

* **Create:** The ability to create tables
* **Read:** The ability to get data from tables
* **Update:** The ability to change values within tables
* **Delete:** The most dangerous ability, _the ability delete data, tables, rows, and colum&#x6E;_&#x73;

We have focused a lot on **Reading** data from tables; this chapter will do basic insertion of data.

## SQL Query Format

```sql
INSERT INTO table_name (column1, column2, column3)
VALUES (value1, value2, value3);
```

* When using the `INSERT` query, you must specify a table that exists in your SQL database
* The values that you want to insert should line up with the columns that it should go into
* It is imperative to understand that we are adding a row of data when **INSERTING**

### Example

Examine the following `employee` table:

| id | name          | position          |
| -- | ------------- | ----------------- |
| 1  | John Doe      | Software Engineer |
| 2  | Jane Smith    | Product Manager   |
| 3  | Alice Johnson | UX Designer       |

Our goal is to insert the following employee:

* ID: 4
* Name: Lil Kid
* Position: Junior Developer

**The query would look like:**

```sql
INSERT INTO employee (id, name, position)
VALUES (4, 'Lil Kid', 'Junior Developer');
```

**In Python, it would look like:**

```python
# assuming that cursor object exists already ...
cursor.execute(
    '''
    INSERT INTO employees (id, name, position)
    VALUES (?, ?, ?)
    ''', 
    (4, 'Lil Kid', 'Junior Developer')
)
```

The `execute()` method is going to be using two argument inputs.

* The query as a long string
* A tuple that contains the value to be inserted

### The reason for using `(?, ?, ?)` in our query

The question marks will act as a placeholder and they will use the values we provide within our 2nd argument in order.

This is to prevent a topic called "[**SQL Injection Attacks**](https://www.w3schools.com/sql/sql_injection.asp)**"**
