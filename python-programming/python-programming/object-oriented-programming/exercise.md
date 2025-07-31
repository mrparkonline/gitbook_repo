# Exercise

## 1) Book Data

Create a book class to represent that a book contains

* title
* author
* pages
* year
* type (for example: fiction, non-fiction)

Solution Link

## 2) Create a Circle Class

* Attributes:&#x20;
  * radius
  * diameter
* Methods:&#x20;
  * get\_radius -OR- write a getter
  * get\_diameter -OR- write a getter
  * get circumference
  * get area
  * make it printable

[Solution Link](https://github.com/mrparkonline/ics4u_2023F/blob/main/oop/2024/circle.py)

## 3) Inventory Items at a Store

An item in a store has:

* Product Name
* Product Price
* Product Description
* Product Quantity

Based on this list, create an item class for a store product.&#x20;

[Solution Link](https://github.com/mrparkonline/ics4u_2023F/blob/main/oop/2024/item.py)

## 4) Rock Paper Scissors

Create a `RPS` class that contains attributes and methods to run a game of rock paper and scissors.

Solution Link

## 5) Stack

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

A [**`stack`**](https://en.wikipedia.org/wiki/Stack_\(abstract_data_type\)) is a data structure that has two main features:

* `Push` -> adds an element to the collection
* `Pop` -> removes the most recently added element

A common use of stack is the "undo" function. By removing the most recently made edits on a text file, we can go back to a previous state.

### Stack's Attribute

* Storage -> for simplicity, it will be a read only list attribute
* Length -> tracking the size of the Stack
* IsEmpty -> True when storage is empty

### Stack's Methods

* Push
* Pop
* Peek -> read-only view of what is at the top of the stack

_All of stack operations are `O(1)` with a space complexity of `O(n)`_

Solution Link
