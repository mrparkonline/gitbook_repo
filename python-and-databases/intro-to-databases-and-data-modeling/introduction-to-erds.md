# Introduction to ERDs

An **Entity-Relationship Diagram (ERD)** is a visual representation of the entities, attributes, and relationships within a database.&#x20;

ERDs are used to model the logical structure of databases and help in designing and understanding the database schema[^1].

## Key Terms

**Entities**

An **entity** is a real-world object or concept that can have data stored about it.&#x20;

* Entities are represented as **`rectangles`** in ERDs.&#x20;
* Examples include `Customer`, `Order`, and `Product`.

**Attributes**

**Attributes** are properties or characteristics of an entity.&#x20;

* They are represented as **`ovals`** connected to their respective entities.&#x20;
* Examples include `CustomerName`, `OrderDate`, and `ProductPrice`.

[**Relationships**](introduction-to-erds.md#types-of-relationships)

**Relationships** describe how entities interact with each other.&#x20;

* They are represented as **`diamonds or lines`** connecting entities.&#x20;
* Relationships can be _one-to-one, one-to-many, or many-to-many_.

## Types of Relationships

**One-to-One (1:1)**

In a one-to-one relationship, each instance of Entity A is associated with one instance of Entity B, and vice versa.&#x20;

For example, each `Person` has one `Passport`, and each `Passport` is assigned to one `Person`.



**One-to-Many (1:M)**

In a one-to-many relationship, each instance of Entity A can be associated with multiple instances of Entity B, but each instance of Entity B is associated with only one instance of Entity A.&#x20;

For example, one `Customer` can place many `Orders`, but each `Order` is placed by one `Customer`.



**Many-to-Many (M:N)**

In a many-to-many relationship, each instance of Entity A can be associated with multiple instances of Entity B, and vice versa.&#x20;

For example, `Students` can enroll in many `Courses`, and each `Course` can have many `Students`.



[^1]: a representation of a plan or theory in the form of an outline or model.
