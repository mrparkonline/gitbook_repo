# Removing Items from a List

There are many ways to remove values from a list, we will be exploring most of them.

With removal, there are a lot of dangerous situations that can occur. It is advised to understand each technique before thinking about value removals.

#### Removal by a Target Value <a href="#removal-by-a-target-value" id="removal-by-a-target-value"></a>

`.remove(target)` method will remove the **first occurance** of the targetted value if it exists in the list.

If the target\_value doesn’t exist, it will produce an **error**.

```python
# .remove() example

a_list = ['apple', 'oranges', 'kiwi', 'honeydew', 'apple']
a_list.remove('apple')
a_list.remove('kiwi')

print('a_list:', a_list)
```

```
a_list: ['oranges', 'honeydew', 'apple']
```

#### Removal by Index <a href="#removal-by-index" id="removal-by-index"></a>

`.pop(target_index)` will remove a value located at the `target_index` and **RETURN THE VALUE**.

* If the target\_index goes beyond the list size, it will produce an error.
* `pop()` without an target index returns and removes the last value

```python
# .pop() example

a_list = ['apple', 'oranges', 'kiwi', 'honeydew', 'apple']
removed1 = a_list.pop()
a_list.pop(2)


print('a_list:', a_list)
print('removed1:', removed1)
```

```
a_list: ['apple', 'oranges', 'honeydew']
removed1: apple
```

#### Removing All Items in a List <a href="#removing-all-items-in-a-list" id="removing-all-items-in-a-list"></a>

`.clear()` is a method that will empty out its list.

```python
# .clear() example

a_list = ['apple', 'oranges', 'kiwi', 'honeydew', 'apple']
a_list.clear()

print('a_list:', a_list)
```

```
a_list: []
```

#### Introduction to `del` <a href="#introduction-to-del" id="introduction-to-del"></a>

`del` is used to delete objects in Python. _The concepts of “objects” are discussed in a future course!_

_`del` can delete an entire instance of a list_

```python
# del example 1

a_list = ['apple', 'oranges', 'kiwi', 'honeydew', 'apple']
del a_list

print('a_list:', a_list)
```

```
---------------------------------------------------------------------------

NameError                                 Traceback (most recent call last)

<ipython-input-5-eb3269d4b4cb> in <module>
      4 del a_list
      5
----> 6 print('a_list:', a_list)


NameError: name 'a_list' is not defined
```

Notice that since the variable was deleted, we get an error say that the `a_list` was never created.

_`del` can delete a single item in a list by indexing_

```python
# del example 2

a_list = ['apple', 'oranges', 'kiwi', 'honeydew', 'apple']
del a_list[1]
del a_list[-1]

print('a_list:', a_list)
```

```
a_list: ['apple', 'kiwi', 'honeydew']
```

There are no errors here since we are only deleting single items from the list.

_`del` can delete via slicing_

```python
# del example 3

a_list = ['apple', 'oranges', 'kiwi', 'honeydew', 'apple']
del a_list[0:3]

print('a_list:', a_list)
```

```
a_list: ['honeydew', 'apple']
```

Notice that the first three items were deleted from a\_list.

### MAJOR DANGER: Deletion During Iteration <a href="#major-danger-deletion-during-iteration" id="major-danger-deletion-during-iteration"></a>

It is very common for beginner programmers to _delete while iterating the targeted list_.

**Observe:**

```python
# Example of bad practice

a_list = ['apple', 'oranges', 'kiwi', 'honeydew', 'apple']
for value in a_list:
    if value == 'kiwi':
        a_list.remove(value)

    print('value is currently:', value)
print('-'*64)

print('a_list:', a_list)
```

```
value is currently: apple
value is currently: oranges
value is currently: kiwi
value is currently: apple
----------------------------------------------------------------
a_list: ['apple', 'oranges', 'honeydew', 'apple']
```

**Explanation:**

* The print statement inside the iteration prints ‘kiwi’
* The print statement of ‘kiwi’ should have been impossible since ‘kiwi’ was deleted
* This happens because _a for loop never re-checks the value of a\_list_

**Recommendations:**

1. Use while loops and index-based deletion
2. Make a copy of the list, execute deletion on the copy
