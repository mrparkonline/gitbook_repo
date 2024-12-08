# Exercise

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

## Aggregate Queries with Grouping Exercise

1. Display the total number of each product sold
2. Display the total number of times a customer placed an order
3. Display the minimum, maximum, and average amount of each product sold
4. Display the frequency of each product bought by a customer
