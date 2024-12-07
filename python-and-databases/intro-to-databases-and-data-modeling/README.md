# Intro to Databases & Data Modeling

## What is a Database?

A **database** is an organized collection of data that is stored and accessed electronically.&#x20;

Databases are designed to manage large amounts of information efficiently and allow for quick retrieval, insertion, updating, and deletion of data. They are typically managed by Database Management Systems.

In this chapter we will be learning about **Structured Query Language** (SQL) to interact with a database.

In [**SQL**](https://en.wikipedia.org/wiki/SQL), data is organized into tables, which consist of rows and columns. Each **row** represents a single record, while each **column** represents a specific attribute of that record. This structure allows for efficient data storage, retrieval, and manipulation.

## Important Terminologies

**Table**: A table is a collection of related data organized in a grid of rows and columns.&#x20;

Each table in a database represents a specific entity, such as customers, products, or orders.

**Fields**: A field is a single piece of information or data value stored within a record or row.&#x20;

Fields act as containers that hold data of a particular type, such as text, numbers, or dates.

* _In the context of a table, fields are synonymous with columns._
* HOWEVER, we can also use the word `"field"` to represent the values within a record

**Records**: A record is a collection of fields that contain data about a specific entity.&#x20;

In a table, a record is typically stored as a row.&#x20;

Each record includes all the data for one entity instance.

**Attributes**: Attributes are the characteristics or properties that define and describe entities within a database.

Each attribute corresponds to a column in a table and holds specific data values for an instance of an entity.

### Example

| StudentID | Name  | Age | Major            |
| --------- | ----- | --- | ---------------- |
| 1         | Alice | 20  | Computer Science |
| 2         | Bob   | 22  | Mathematics      |
| 3         | Carol | 21  | Physics          |

* The diagram above is a table called `StudentData`
* There are 3 `records` (rows)
* There are 4 `attributes` called: `StudentID, Name, Age, Major`
* _The record with `StudentID` of `1` has the following fields:_
  * `1, Alice, 20, Computer Science`

### Databases vs. Spreadsheets

| Feature                               | Database                                                              | Spreadsheet                                           |
| ------------------------------------- | --------------------------------------------------------------------- | ----------------------------------------------------- |
| Structure                             | Highly structured with tables, rows, and columns.                     | Less structured, often used for individual data sets. |
| Data Volume/size                      | Can handle large volumes of data efficiently.                         | Best for smaller data sets.                           |
| Data Integrity                        | Enforces data integrity and relationships between tables.             | Limited data integrity features.                      |
| Concurrency (Multiple access at once) | Supports multiple users accessing and modifying data simultaneously.  | Limited support for concurrent access.                |
| Complex Queries                       | Can perform complex queries and transactions.                         | Limited querying capabilities.                        |
| Automation                            | Supports automation through triggers, stored procedures, and scripts. | Basic automation through formulas and macros.         |

#### Advantages of Databases

1. **Scalability**: Databases can handle large volumes of data and scale as needed.
2. **Data Integrity**: Ensures data accuracy and consistency through constraints and relationships.
3. **Security**: Provides robust security features to protect sensitive data.
4. **Concurrent Access**: Allows multiple users to access and modify data simultaneously without conflicts.
5. **Complex Queries**: Supports complex queries and data manipulation through SQL.
6. **Backup and Recovery**: Offers advanced backup and recovery options to prevent data loss.

#### Advantages of Spreadsheets

1. **Ease of Use**: User-friendly interface, easy to set up and use without extensive training.
2. **Flexibility**: Great for ad-hoc analysis and small data sets.
3. **Visualization**: Built-in tools for creating charts and graphs.
4. **Cost**: Often more cost-effective for small-scale data management tasks.
5. **Accessibility**: Easily accessible and shareable, especially with cloud-based solutions like Google Sheets.
