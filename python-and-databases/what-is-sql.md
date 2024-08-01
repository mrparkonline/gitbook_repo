# What is SQL?

## SQL (Structured Query Language)&#x20;

SQL is a standardized programming language used to manage and manipulate relational databases. It is widely used for querying, updating, and managing data stored in a database. SQL allows users to perform a variety of operations on the data, such as retrieving specific information, inserting new records, updating existing records, and deleting records.

### What is a Relational Database?

A relational database is a type of database that organizes data into structured tables with rows and columns.&#x20;

Each table represents a specific entity, and the columns define the attributes of that entity, while the rows contain the data entries or records. The relational model allows data to be easily queried, manipulated, and managed using SQL (Structured Query Language).

One of the key features of relational databases is the use of **relations** (or tables) to establish connections between different data entities.&#x20;

These relationships are often defined using **foreign keys**, which are references to primary keys (unique identifiers) in other tables. This structure enables efficient data retrieval and integrity, as well as the ability to enforce constraints and maintain data consistency.&#x20;

Popular relational database management systems (RDBMS) include MySQL, PostgreSQL, Oracle, and Microsoft SQL Server.

### [SQLite](https://www.sqlite.org/)

SQLite is a lightweight, embedded relational database management system that comes bundled with Python. With SQLite, databases are stored in a single file, making them easy to manage and share. The Python Standard Library includes the `sqlite3` module, allowing for easy integration and interaction with SQLite databases using standard SQL queries.

### What is query?

A query in SQL is a request for data or information from a database. It is typically written in SQL syntax and is used to perform various operations, such as retrieving specific data, inserting new records, updating existing records, or deleting records.

The most common type of SQL query is the `SELECT` statement, which retrieves data from one or more tables based on specified criteria.
