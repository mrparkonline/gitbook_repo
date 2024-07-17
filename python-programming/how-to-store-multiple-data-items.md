# How to Store Multiple Data Items

## Scenario

As a programmer, there are instances where you would need a single variable to hold multiple values. There are many answers to this situation because there are different designed solutions to different scenarios of this problem.

There are many built-in data types (list, set, and dictionary) that can help us that best suits the given situation.

We will be looking at 3 basic practices.

### Option 1 - Using [lists](../02-programming-in-python/tuples-and-lists/)

* [ ] Items are not consistent in data type
* [ ] Items can repeat
* [ ] Item location / address does not matter; therefore, it will be just ordered based on time of insertion
* [ ] Items should be available to be accessed based on their index location
* [ ] Items at certain index should be modifiable

```python
# Example of a list data

example = ['Marshall', 'Park', 4, ['Freya', 'Goji'], 'White']
```

A `list` in python can contain any type of data.&#x20;

Each item added will have a numeric index (starting at 0).

* `example[0]` will contain a String data of `'Marshall'`
* `example[3]` will contain a List data containing `['Freya,' 'Goji']`

```python
# Example being modified

example = ['Marshall', 'Park', 4, ['Freya', 'Goji'], 'White']

example[2] = 5 # now example is: ['Marshall', 'Park', 5, ['Freya', 'Goji'], 'White']
```

Lists are built-in data type in Python that offers strong set of operations and methods to provide a way to have data collection.

### Option 2 - Using [sets](../02-programming-in-python/sets.md)

#### Main Reason: To check if some item exists, checking against a set is faster than checking against a list

* [ ] Sets can handle different data types, but most often each item in a set should be a same data type
  * [ ] Sets also cannot contain [mutable data types](https://realpython.com/python-mutable-vs-immutable-types/)
* [ ] There should be no duplicates; each items are unique
* [ ] Order of insertion does not matter
* [ ] When you need an implementation of a [mathematical set](https://en.wikipedia.org/wiki/Set\_\(mathematics\)) so that you can perform [set operations](https://www.cuemath.com/algebra/operations-on-sets/) ([Python documentation link](https://docs.python.org/3.8/library/stdtypes.html#set-types-set-frozenset))
* [ ] We can convert a list with duplicate items to set to remove duplicates
* [ ] Items are still addable and removable in a set

```python
# Example of a set

allergies = {'Dairy', 'Shellfish', 'Peanuts'}

list_allergies = ['Dairy', 'Shellfish', 'Peanuts']

print("Is the person allergic to dust?")
print("Dust" in allergies) # Outputs: False
print("Dust" in list_allergies) # Outputs: False
```

The code above currently has two collection of data: a set and a list.

It is currently trying to see if the person is allergic to `dust` given the two collections with same item values.

With respect to performance (_speed of the program_), the `set` based collection will outperform the `list`.

**Reasoning:**

* Because each individual item in a set is unique, Python generates an integer address for each item.&#x20;
  * This is the reason that sets do not have duplicates; duplicates would generate the same integer address. This concept of integer addressing is called [hashing](https://www.geeksforgeeks.org/what-is-hashing/).
* When we are checking if `dust` is an item in the set of of `allergies` by executing: **`"Dust" in allergies`**, Python would hash the value of `dust` and try to access the location of it from `allergies`. Since that address is not part of the set, it can immediately return a value of **`False`**
* When `dust` is being searched through the list, Python starts the search from the beginning of the list, and it compares every item against `dust` until found. If it is never found, then we reach the end of the list to return `False`

Therefore, a set would need to do a single hashing operation to see if that value is in the set or not. However, a list would have to check every single value against the searching value to see if it exists in the list. As the size of the list grows, the number of comparisons Python needs to do would be far larger than the number of comparisons a set would have done.

### Option 3 - Countable Unique Items

For this situation, let's look at an example first.

```python
# Unique, but countable

inventory = {
    'pencil' : 2,
    'pen' : 1,
    'erasor' : 1
    'white-out' : 1,
}
```

The code above is an example of using a [dictionary](../02-programming-in-python/dictionary.md).

A dictionary will always store two types of information for each item in its collection.

1. **Address** (commonly known as "key") -> Dictionary allows us to use immutable customized hashing for our items in the dictionary to act as an index for dictionary items.
2. **Value** -> Dictionary allows us to associate any type of data located at our custom address

In Python programming, dictionaries are a way to create a key+value pairs of data.
