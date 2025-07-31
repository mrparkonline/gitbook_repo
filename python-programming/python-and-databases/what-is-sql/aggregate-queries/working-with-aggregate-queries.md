# Working with Aggregate Queries

_Lesson 5 Directory_

## This Tutorial's Database: `Orders.db`

`Orders.db` contains a table called `Orders`

`Orders` Table Attributes:

* `OrderID` INTEGER PRIMARY KEY
* `ProductName` TEXT NOT NULL
* `OrderSize` INTEGER NOT NULL
* `CustomerID` INTEGER NULL

**First 10 values within the dataset**

```
(1, 'Oranges', 32, None)
(2, 'Pasta', 41, None)   
(3, 'Broccoli', 51, None)
(4, 'Apples', 36, 8)     
(5, 'Apples', 44, 17)    
(6, 'Spinach', 95, 1)    
(7, 'Oranges', 47, 18)   
(8, 'Carrots', 13, None) 
(9, 'Onions', 5, None)
(10, 'Milk', 56, None)
```

## Exercises

Determine the query for the following analysis.

1. Determine the total number of records within the `orders` table
2. Determine the number of unique products sold
3. Determine the number of our customer base
4. Determine the total number of goods sold
5. Determine the average amount of goods sold
6. Determine the single record with the most items sold
7. Determine the single record with the least items sold
