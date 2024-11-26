# Database Normalization

**Database normalization** is the process of organizing the fields and tables of a relational database to minimize redundancy and dependency.&#x20;

{% hint style="info" %}
The goal is to ensure that each piece of data is stored only once, which helps maintain data integrity and makes the database more efficient.
{% endhint %}

**Reducing Data Redundancy**

Normalization helps eliminate duplicate data by ensuring that each piece of information is stored in only one place. This reduces the amount of storage required and prevents inconsistencies that can arise when the same data is updated in multiple places.

**Improving Data Integrity**

By organizing data into related tables and defining relationships between them, normalization ensures that data remains accurate and consistent. For example, if a customer's address is stored in one table, any changes to the address need to be made only once, reducing the risk of errors.

## Normal Forms

Normalization is typically carried out through a series of steps known as **normal forms**.

**First Normal Form (1NF)**&#x20;

* Ensures that the table has a primary key and that all columns contain atomic (indivisible) values.&#x20;
  * **There should also be no repeating groups or arrays.**

{% hint style="danger" %}
**Atomic Values**

"identify something _**as small as possible**"_

Example of Values that are not atomic:

* Contact Information: `123-456-7890, john@example.com`

This is not atomic because the value in this column called `ContactInformation` contains multiple values at once: a phone number and an email address.

Their information should have been separated into multiple columns of `PhoneNumber` and `Email`
{% endhint %}

| ID | Name | Phone1       | Phone2       | Phone3       |
| -- | ---- | ------------ | ------------ | ------------ |
| 1  | John | 123-456-7890 | 234-567-8901 | 345-678-9012 |
| 2  | Jane | 987-654-3210 | NULL         | NULL         |

{% hint style="warning" %}
**No Repeating Groups or Arrays**

* In the table above: columns (`Phone1, Phone2, Phone3`) represent a repeating group because **they store similar information**
* For the table to achieve 1NF; create separate table for customers and phone numbers.
{% endhint %}

**`Customers Table`**

| ID | Name |
| -- | ---- |
| 1  | John |
| 2  | Jane |

**`PhoneNumbers Table`**

| ID | PhoneNumber  |
| -- | ------------ |
| 1  | 123-456-7890 |
| 1  | 234-567-8901 |
| 1  | 345-678-9012 |
| 2  | 987-654-3210 |

**Second Normal Form (2NF)**

* Achieved when the table is in 1NF and all non-key columns are fully dependent on the primary key.

**Third Normal Form (3NF)**

* Achieved when the table is in 2NF and all columns are dependent only on the primary key, not on other non-key columns.

### Normalizing a Table Example

| OrderID | Name        | ItemsOrdered            | TotalAmount |
| ------- | ----------- | ----------------------- | ----------- |
| 1       | John Doe    | Apple, Oranges          | 15          |
| 2       | Jane Smith  | Bananas, Grapes, Apples | 20          |
| 3       | Bob Johnson | Oranges                 | 5           |

#### 1NF -> _Make sure that each column contains atomic values and no repeating groups_

Result:

| OrderID | Name        | ItemOrdered | TotalAmount |
| ------- | ----------- | ----------- | ----------- |
| 1       | John Doe    | Apples      | 15          |
| 1       | John Doe    | Oranges     | 15          |
| 2       | Jane Smith  | Bananas     | 20          |
| 2       | Jane Smith  | Grapes      | 20          |
| 2       | Jane Smith  | Apples      | 20          |
| 3       | Bob Johnson | Oranges     | 5           |

#### 2NF -> _Remove Partial Dependencies_

* non-key attributes should depend on primary key
  * Make `TotalAmount` depend on `OrderID`
  * Split the table into `Orders(OrderID, Name, TotalAmount)` and `OrderItems(OrderID, ItemOrdered)`

**`Orders Table`**

| OrderID | Name        | TotalAmount |
| ------- | ----------- | ----------- |
| 1       | John Doe    | 15          |
| 2       | Jane Smith  | 20          |
| 3       | Bob Johnson | 5           |

**`OrderItems Table`**

| OrderID | ItemOrdered |
| ------- | ----------- |
| 1       | Apples      |
| 1       | Oranges     |
| 2       | Bananas     |
| 2       | Grapes      |
| 2       | Apples      |
| 3       | Oranges     |

#### 3NF -> _Remove Transitive dependencies_

* Non-key attributes should not depend on other non-key attributes.
  * Both tables: `Orders` and `OrderItem` are already 3NF.

### Example Table that is 2NF but not 3NF

| StudentID | CourseID | CourseName | InstructorID | InstructorName |
| --------- | -------- | ---------- | ------------ | -------------- |
| 1         | 101      | Math       | 1001         | Dr. Smith      |
| 1         | 102      | History    | 1002         | Dr. Brown      |
| 2         | 101      | Math       | 1001         | Dr. Smith      |
| 2         | 103      | Science    | 1003         | Dr. White      |

1NF Properties:

* The table is atomic because each attribute in a record holds one value
* There are no repetitive columns

2NF Properties

* All non-key columns are dependent on composite primary keys (StudentID, CourseID)

**This table fails to be 3NF because `InstructorName depends on InstructorID` not being dependent on both `StudentID and CourseID`**

To normalize this table to 3NF, we need to remove the **transitive dependency** by creating a separate table for instructors:

**`StudentsCourses Table:`**

| StudentID | CourseID | CourseName | InstructorID |
| --------- | -------- | ---------- | ------------ |
| 1         | 101      | Math       | 1001         |
| 1         | 102      | History    | 1002         |
| 2         | 101      | Math       | 1001         |
| 2         | 103      | Science    | 1003         |

**`Instructors Table:`**

| InstructorID | InstructorName |
| ------------ | -------------- |
| 1001         | Dr. Smith      |
| 1002         | Dr. Brown      |
| 1003         | Dr. White      |
