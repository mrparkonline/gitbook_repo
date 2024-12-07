# AGGREGATE Queries

Aggregate queries in SQL use aggregate functions to perform calculations on a set of values, returning a single value.

{% hint style="info" %}
Aggregate queries are often paired with `SELECT` queries

These aggregate queries perform calculations on a selected attribute and return a single value, which is useful for summarizing and analyzing data.
{% endhint %}

The common queries we will use are the following:

* **`COUNT()`**: Returns the number of rows.
* **`SUM()`**: Returns the total sum of a numeric column.
* **`AVG()`**: Returns the average value of a numeric column.
* **`MIN()`**: Returns the smallest value in a column.
* **`MAX()`**: Returns the largest value in a column

Aggregate queries are useful for:

* Exploring a database that you have not seen
  * This is because you can infer characteristics of a table without reading individual records
* Looking at behaviours of an attribute
  * By counting distinct values in an attribute, you can the total distinct number of items that are contained in the attribute
  * The summation of all values in an attribute can be important conclusions
    * Example: sum of all the amount of products sold
  * An average tells you a common value within the attribute
  * The minimum value tells you the lowest possible value within the attribute
  * The maximum value tells you the highest possible value within the attribute
* Counting NULL values in an attribute
  * This is important because if records have some attributes not represented, it could affect the integrity of the dataset
