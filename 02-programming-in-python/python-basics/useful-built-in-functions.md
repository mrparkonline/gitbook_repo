# Useful Built-in Functions

1. **round()**: The `round()` function is used to round a number to a specified number of decimal places.&#x20;

It takes one required argument, the number to be rounded, and an optional argument that specifies the number of decimal places (default is 0). The function returns a floating-point number.

```python
#Example
num = 3.14159
rounded_num = round(num, 2)
print(rounded_num)  # Output: 3.14
```

2. **chr()**: The `chr()` function returns a string representing a character whose Unicode code point is the specified integer.&#x20;

It takes an integer argument and returns the corresponding character.

```python
#Example
unicode_num = 65
character = chr(unicode_num)
print(character)  # Output: 'A'
```

3. **ord()**: The `ord()` function returns an integer representing the Unicode character.&#x20;

It takes a single character as an argument and returns the Unicode code point of that character.&#x20;

```python
# Example
character = 'A'
unicode_num = ord(character)
print(unicode_num)  # Output: 65
```

4. **len()**: The `len()` function is used to determine the length or size of an object.&#x20;

It returns the number of items in an object such as a string, list, tuple, or dictionary.

```python
# Example
my_string = "Hello, World!"
length = len(my_string)
print(length)  # Output: 13
```

5. **min()**: The `min()` function is used to find the minimum value among the given arguments or an iterable object.&#x20;

It can be used with numbers, strings, or other comparable objects.

```python
# Min Example #1
numbers = [4, 7, 2, 9, 1]
minimum = min(numbers)
print(minimum)  # Output: 1
```

The `min()` function can also take multiple arguments separated by a comma to determine the minimum value from variables or multiple data objects.

```python
# Min Example #2
x = 13
y = 11
z = 12
print(min(x, y, z)) # Output is 11 from variable y
```

6. **max()**: The `max()` function is used to find the maximum value among the given arguments or an iterable object.&#x20;

It works similarly to `min()` but returns the maximum value instead. `max()` can also take multiple arguments as well.

```python
# Max Example
numbers = [4, 7, 2, 9, 1]
maximum = max(numbers)
print(maximum)  # Output: 9
```

7. **sum()**: The `sum()` function is used to calculate the sum of all elements in an [**iterable**](#user-content-fn-1)[^1]/sequence, such as a list or tuple.&#x20;

It takes an iterable as an argument and returns the sum of its elements. The items of each iterable must be addable.

```python
# Example
numbers = [1, 2, 3, 4, 5]
total = sum(numbers)
print(total)  # Output: 15
```

These are some of the commonly used functions in Python that perform specific operations, such as rounding, character conversions, length calculation, finding minimum and maximum values, and summing elements.



[^1]: An iterable is any Python object capable of returning its members one at a time, permitting it to be iterated over in a for-loop.\
    \
    Lists, Tuples, Strings, Sets and Dictionaries are examples of an iterable object
