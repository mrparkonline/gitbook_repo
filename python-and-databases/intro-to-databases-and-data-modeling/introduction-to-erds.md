# Introduction to ERDs

{% embed url="https://www.youtube.com/watch?v=xsg9BDiwiJE" %}

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

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption><p>Relationships</p></figcaption></figure>

**One-to-One (1:1)**

In a one-to-one relationship, each instance of Entity A is associated with one instance of Entity B, and vice versa.&#x20;

For example, each `Person` has one `Passport`, and each `Passport` is assigned to one `Person`.

**One-to-Many (1:M)**

In a one-to-many relationship, each instance of Entity A can be associated with multiple instances of Entity B, but each instance of Entity B is associated with only one instance of Entity A.&#x20;

For example, one `Customer` can place many `Orders`, but each `Order` is placed by one `Customer`.

**Many-to-Many (M:N)**

In a many-to-many relationship, each instance of Entity A can be associated with multiple instances of Entity B, and vice versa.&#x20;

For example, `Students` can enroll in many `Courses`, and each `Course` can have many `Students`.

## Three Levels/Types of ERD

1. Conceptual (High Level, General Purpose)
2. Logical (Focuses more on the structure of data)
3. Physical (Most detail often the schematics to an actual database)

### Conceptual (Business)

* Focuses on high-level relationships between entities.
* Used in the initial stages of database design to capture essential entities and their relationships.
* Helps stakeholders understand the scope and requirements of the database system.

### Logical (Designers)

* Used to translate the conceptual model into a relational database schema.
* Specifies attributes for each entity, defines cardinality/relationships (one to one, one to many) and participation(optional vs required) attributes.
* Provides a detailed view of the database schema, including primary and foreign keys

### Physical (Developer)

* Represents the actual implementation of the database on a specific DBMS in order to to build, optimize, and maintain the physical database schema.
* Includes details such as data types, indexes, storage options, and constraints tailored to the chosen DBMS.

[^1]: a representation of a plan or theory in the form of an outline or model.
