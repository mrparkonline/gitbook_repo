# Iterable Functions w/ For Loops

We will be exploring more functions similar to `range()` where they also return an iterable sequence that we can iterate through with a for loop

## 1. [`sorted()`](https://docs.python.org/3/library/functions.html#sorted) function <a href="#1-sortedhttpsdocspythonorg3libraryfunctionshtmlsorted-function" id="1-sortedhttpsdocspythonorg3libraryfunctionshtmlsorted-function"></a>

The `sorted()` function will return a sorted list in order from least to greatest from a sortable sequence.

* For strings, they follow their [ASCII table value order](http://www.asciitable.com/).
* For lists, it will depend on the datatype of each item. It is recommended that all the items have the same data type in the list if you are using sorted.
* The result of a `sorted()` is printable as it returns a list

{% tabs %}
{% tab title="Code" %}
```python
# Using sorted on a string

example = 'Computer Science!'
example_sorted = sorted(example)
print('Sorted Version:', example_sorted)

for item in example_sorted:
    print('    -- Current item:', item)
```
{% endtab %}

{% tab title="Output" %}
```
Sorted Version: [' ', '!', 'C', 'S', 'c', 'c', 'e', 'e', 'e', 'i', 'm', 'n', 'o', 'p', 'r', 't', 'u']
    -- Current item:  
    -- Current item: !
    -- Current item: C
    -- Current item: S
    -- Current item: c
    -- Current item: c
    -- Current item: e
    -- Current item: e
    -- Current item: e
    -- Current item: i
    -- Current item: m
    -- Current item: n
    -- Current item: o
    -- Current item: p
    -- Current item: r
    -- Current item: t
    -- Current item: u
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Code" %}
```python
# Using sorted on a list of numbers but in reverse

numbers = [2,3,5,7,11,13]

for number in sorted(numbers, reverse=True):
    print('Current Number:', number)

# NOTE: if reverse is not a given argument, it will be assumed as False
```
{% endtab %}

{% tab title="Output" %}
```
Current Number: 13
Current Number: 11
Current Number: 7
Current Number: 5
Current Number: 3
Current Number: 2
```
{% endtab %}
{% endtabs %}

## 2. [`enumerate()`](https://docs.python.org/3/library/functions.html#enumerate) function <a href="#2-enumeratehttpsdocspythonorg3libraryfunctionshtmlenumerate-function" id="2-enumeratehttpsdocspythonorg3libraryfunctionshtmlenumerate-function"></a>

The `enumerate()` function will pair the index for each item in the given sequence argument. This allow us to do a special type of for loop that involves [variable unpacking](https://www.geeksforgeeks.org/unpacking-a-tuple-in-python/).

* The result of `enumerate()` is not printable

{% tabs %}
{% tab title="Code" %}
```python
# Using enumerate() with a list of fruits

fruits = ['Apple', 'Banana', 'Kiwi', 'Strawberry']

for i, fruit in enumerate(fruits):
    print('Current index:', i)
    print('Current fruit:', fruit)

    if i != len(fruits) - 1:
        print('--')
```
{% endtab %}

{% tab title="Output" %}
```
Current index: 0
Current fruit: Apple
--
Current index: 1
Current fruit: Banana
--
Current index: 2
Current fruit: Kiwi
--
Current index: 3
Current fruit: Strawberry# enumerate() on a string
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Code" %}
```python
# enumerate() on a string

word = 'Hello'

for i, character in enumerate(word):
    print(i, character)
```
{% endtab %}

{% tab title="Output" %}
```
0 H
1 e
2 l
3 l
4 o
```
{% endtab %}
{% endtabs %}

## 3. [`reversed()`](https://docs.python.org/3/library/functions.html#reversed) function <a href="#3-reversedhttpsdocspythonorg3libraryfunctionshtmlreversed-function" id="3-reversedhttpsdocspythonorg3libraryfunctionshtmlreversed-function"></a>

The `reversed()` is a simple function that reverses any given sequence.

* The result of `reversed()` is not printable

{% tabs %}
{% tab title="Code" %}
```python
# Using reversed() with a list of fruits

fruits = ['Apple', 'Banana', 'Kiwi', 'Strawberry']

for fruit in reversed(fruits):
    print('Current fruit:', fruit)
```
{% endtab %}

{% tab title="Output" %}
```
Current fruit: Strawberry
Current fruit: Kiwi
Current fruit: Banana
Current fruit: Apple
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Code" %}
```python
# Using reversed() on a string

word = 'Do geese see God?'

for character in reversed(word):
    print(character)
```
{% endtab %}

{% tab title="Output" %}
```
?
d
o
G

e
e
s

e
s
e
e
g

o
D
```
{% endtab %}
{% endtabs %}
