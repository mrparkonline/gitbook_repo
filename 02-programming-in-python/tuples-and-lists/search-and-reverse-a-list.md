# Search & Reverse a List

#### Finding a Targetted Value <a href="#finding-a-targetted-value" id="finding-a-targetted-value"></a>

`.index(target, start, end)` method will find the first occurance of the target if it exists.

* If the target does not exist, it raises and error
* Both `start` and `end` arguments are **optional**
  * They act like slicing mechanism, we can look for the index of a value within such boundaries

```python
# .index() example

a_list = ['apple', 'oranges', 'kiwi', 'honeydew', 'apple']

print("a_list.index('oranges'):", a_list.index('oranges'))
print("a_list.index('kiwi', 1, 5):", a_list.index('kiwi', 1, 5))
```

```
a_list.index('oranges'): 1
a_list.index('kiwi', 1, 5): 2
```

#### Counting the Number of Occurrence of a Target <a href="#counting-the-number-of-occurrence-of-a-target" id="counting-the-number-of-occurrence-of-a-target"></a>

`.count(target)` method counts the number of times target occurs.

* If target does not exist, returns 0

```python
# .count() example

a_list = ['apple', 'oranges', 'kiwi', 'honeydew', 'apple']

print("a_list.index('oranges'):", a_list.count('oranges'))
print("a_list.index('apple'):", a_list.count('apple'))
print("a_list.index('strawberry'):", a_list.count('strawberry'))
```

```
a_list.index('oranges'): 1
a_list.index('apple'): 2
a_list.index('strawberry'): 0
```

#### Mutate and Reverse a list <a href="#mutate-and-reverse-a-list" id="mutate-and-reverse-a-list"></a>

`.reverse()` will reverse the order of the items in the list

```python
# .reverse() example

a_list = ['apple', 'oranges', 'kiwi', 'honeydew', 'apple']
a_list.reverse()

print('a_list is now:', a_list)
```

```
a_list is now: ['apple', 'honeydew', 'kiwi', 'oranges', 'apple']
```
