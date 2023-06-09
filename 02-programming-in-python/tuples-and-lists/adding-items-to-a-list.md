# Adding Items to a List

List’s versatility to comes from its ability to contain information and add on information. This lesson covers how to do so.

#### Adding an Item to the End of a List <a href="#adding-an-item-to-the-end-of-a-list" id="adding-an-item-to-the-end-of-a-list"></a>

This is the safest and the recommended way to add values: _add the new value to the end_.

`.append(item)` is method that adds the given item to the end of a list.

```python
# .append() Example

a_list = ['apple', 'oranges']
a_list.append('kiwi')
a_list.append('honeydew')
print('a_list:', a_list)
```

```
a_list: ['apple', 'oranges', 'kiwi', 'honeydew']
```

#### Adding an Item at a Location <a href="#adding-an-item-at-a-location" id="adding-an-item-at-a-location"></a>

This technique can cause potential issues; however, it does exist!

`.insert(location, item)` will add the given item at the specified integer location.

**NOTES:**

* If the location is beyond the size, it will add it to the end
* Location can be negative
* If the location already has a value, it will shift everything at the location onwards to the right to add the item

```python
# .insert() Example

a_list = [2,3,5,7]

a_list.insert(5, 11)
print('a_list.insert(5, 11):', a_list)
a_list.insert(-1, 13)
print('a_list.insert(-1, 13):', a_list)
a_list.insert(2, 4)
print('a_list.insert(2, 4):', a_list)
```

```
a_list.insert(5, 11): [2, 3, 5, 7, 11]
a_list.insert(-1, 13): [2, 3, 5, 7, 13, 11]
a_list.insert(2, 4): [2, 3, 4, 5, 7, 13, 11]
```

#### Combining Lists <a href="#combining-lists" id="combining-lists"></a>

There are multiple ways to combine lists!

1. Manipulate a list with all the value from another at the tail-end.

`.extend(list)` is a method that adds all the items from the given list argument to its list.

```python
# .extend() example

basket = [] # Empty List
fruits = ['apple', 'oranges', 'kiwi', 'honeydew']
vegetables = ['onions', 'garlic', 'spinach']

basket.extend(fruits)
basket.extend(vegetables)
print('basket:', basket)
print('fruits:', fruits)
print('vegetables:', vegetables)
```

```
basket: ['apple', 'oranges', 'kiwi', 'honeydew', 'onions', 'garlic', 'spinach']
fruits: ['apple', 'oranges', 'kiwi', 'honeydew']
vegetables: ['onions', 'garlic', 'spinach']
```

2. Use the `+ operator` to generate a new list

The `+` operator is the _concatenation_ operator much like how strings have one.

Instead of manipulate the left operand, it will return a new list.

```python
# concatenation example

fruits = ['apple', 'oranges', 'kiwi', 'honeydew']
vegetables = ['onions', 'garlic', 'spinach']
baskets = fruits + vegetables

print('basket:', basket)
```

```
basket: ['apple', 'oranges', 'kiwi', 'honeydew', 'onions', 'garlic', 'spinach']
```

3. Preserve the variable but generate a new list `+=` operator

We can also use the `+=` assignment operator to concatenate then assign.

```python
# += example

primes = [2, 3, 5, 7]
primes += [11, 13]

print('primes:', primes)
```

```
primes: [2, 3, 5, 7, 11, 13]
```

#### List Repetition Operation <a href="#list-repetition-operation" id="list-repetition-operation"></a>

`*` operator helps us repeat a list.

**Example:**

```python
a = [1,2,3]
print(a*3)

a *= 3
print(a)
```

```
[1, 2, 3, 1, 2, 3, 1, 2, 3]
[1, 2, 3, 1, 2, 3, 1, 2, 3]
```
