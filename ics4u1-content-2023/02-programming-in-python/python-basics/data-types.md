# Data Types

## Python & Data

In Python, all built-in data that can be used are all considered as objects. The concept of objects will be covered in [a _future chapter_](../../04-object-oriented-programming/class-and-objects-definitions.md)_._ Due to such concept, we must understand the concept of **mutability**.

### Immutability & Mutability

A data object in Python is can be considered either immutable or mutable.&#x20;

* An immutable data **cannot be modified** without recreating the data through an assignment operation
* A mutable data **can be modified** without recreating the data. (It can have its inner content changed without _an assignment operation_)

## Immutable Data Objects

```python
# numeric data
number = 42 # an integer based variable
decimal = 3.14159 # a floating point number based variable
```

**Integer objects** are whole numbers that range from negative infinity to positive infinity. Python will have limitations of the computer system itself.

**Floating Point objects** are decimals of Python; moreover, floating points represent all the real numbers.&#x20;

{% hint style="info" %}
Since classical computers use a binary-number system, it does struggle with decimals. There is a great video that you can watch [**here**](https://www.youtube.com/watch?v=PZRI1IfStY0)**.**
{% endhint %}

```python
# text-based data
birthday = "January 1st 2000"

user_name = 'Jane Doe'

lorem_ipsum = """
"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. 
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. 
Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
"""
```

[**String**](../strings/) objects represent any textual data in Python. To create string data, you must trap the text in either single (`''`) or double quotation marks (`""`).&#x20;

Strings are a powerful object that will come with built-in [_methods_](#user-content-fn-1)[^1] for manipulation and comparison which will be studied later.

Any long-text that you want to preserve formatting we often use triple quotation marks.

{% hint style="info" %}
Some characters will be illegal `(example: "Jane "The Programmer" Doe")` will not be a valid string as there are too many quotation marks in a single line.

**The fix:**

`name = "Jane \"The Programmer\" Doe"`

[**Escape Character**](https://www.w3schools.com/python/gloss\_python\_escape\_characters.asp) can be used to help meditate any issues on adding such illegal characters to strings properly.
{% endhint %}

```python
# Decisional Data: boolean

is_late = False
loop = True
```

Boolean objects represents the concept of logical truth. It can have two possible values: `True` and `False`.&#x20;

Booleans are fundamental in [_decision-making and controlling the flow of programs_](../conditionals/).

```python
# Collection Data 1: Tuple

user = ("Jane Doe", "January 1st 2000", 1)
```

[**Tuple**](../tuples-and-lists/) is _one of many data objects_ that allows multiple items to be stored in a single variable container.

## Mutable Data Objects

Lists, Sets, and Dictionaries are all similar to strings in that they have their respective methods. These are important data objects; therefore, they will be highlighted in their own pages.

```python
# Collection Data 2: List

nums = [3,1,4,1,5,9]
words = ["Hello", "World"]
user = ["Jane Doe", "January 1st, 2000", 1]
```

[**List**](../tuples-and-lists/) objects are a mutable container of any data where we can _dynamically_ add new items, extend it with another list, and remove values from it.&#x20;

```python
# Collection Data 3: Sets

fruits = {"Apple", "Banana", "Strawberry"}
nums = {3,1,4,1,5,9}
```

[**Set**](../sets.md) objects are based on [_mathematical definition of sets_](https://en.wikipedia.org/wiki/Set\_\(mathematics\)). Sets can only contain a single copy of an item (no duplicates allowed), and the items that are immutable. Sets are often used for their _membership operators_ as it is much faster than other data types.

```python
 # Collection Data 4: Dictionary
 
 user = {
     "id" : 1,
     "name" : "Jane Doe",
     "birthday" : "January 1st, 2000"
 }
```

[**Dictionaries**](../dictionary.md) objects are ways to create a collection of key (address) to value pairs. Dictionaries allow you to have a unique address for each of your items for fast retrieval.

## Type Casting

Type casting, also known as type conversion, is the process of converting an object from one data type to another in Python. It allows you to change the interpretation and representation of data. Python provides several built-in functions for type casting, which allow you to convert variables from one type to another.

The following are the type casting function to convert one data to another

* `int()` | will convert to integers if possible, will round down always
* `float()` | will convert to decimals if possible, whole numbers will be given `.0`
* `str()` | will convert any data to string
* `bool()` | will convert any data to a Boolean
* `tuple()` | will convert any sequence like data to a tuple
* `list()` | will convert any sequence like data to a list
* `set()` | will convert any sequence like data to a set, duplicates will be removed, order may be different
* `dict()` | will convert any sequence with a some sort of key value pairing to a dictionary

[^1]: programmed procedure that is defined as part of a class and is available to any object instantiated from that class.
