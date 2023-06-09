---
description: >-
  Strings are our first sequence-like data type that we get to manipulate in
  Python.
---

# String Basics

## Strings <a href="#strings" id="strings"></a>

Strings are a data type in Python 3 that represent sequence of alphanumeric characters and special symbols. Strings will be enclosed with either `'single'` or `"double"` quotations marks to denote them as strings. You cannot mix match the quotations.

**Examples:**

* `"a"` or `'a'`
* `"1"` or `'1'`
* `"0010"` or `'0010'`

#### String Characteristics <a href="#string-characteristics" id="string-characteristics"></a>

* Variables can hold string type values: `last_name = "Park"`
* A string value can be empty: `string_variable = ''`
* A space is considered a non-empty string
* Strings are **comparable**; therefore, you can create boolean expressions when comparing strings
  * `'Hello' == 'hello'` evaluates to False because strings are also case-sensitive (also, the ascii value comparisons are different)

#### String Comparison <a href="#string-comparison" id="string-comparison"></a>

![](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/ASCII-Table-wide.svg/1024px-ASCII-Table-wide.svg.png) **Source:** [**Wikipedia**](https://simple.wikipedia.org/wiki/ASCII#/media/File:ASCII-Table-wide.svg)

Whenever a string needs to be sorted or compared, it follows the ASCII order.

* Numeric Symbols are less than uppercase characters
* Uppercase characters are less than lowercase characters

**Example:**

```python
# Comparing Strings

name1 = 'Jake'
name2 = 'Jane'

print(name1 < name2)
```

```
True
```

**Explanation:** The first two characters of the string are equal; however, we now compare the third characters of `'k'` vs. `'n'`.

`'n'` is considered greater than `'k'`; therefore, `'Jane'` is considered **greater**.

**Determining the ASCII Value of a character**

```python
# Using the built-in ord() function

x = ord('A')
print('ASCII Unicode:', x)

print('ASCII Unicode:', ord('J'))
print('ASCII Unicode:', ord('a'))
print('ASCII Unicode:', ord('k'))
print('ASCII Unicode:', ord('e'))
print('ASCII Unicode:', ord('!'))
```

```
ASCII Unicode: 65
ASCII Unicode: 74
ASCII Unicode: 97
ASCII Unicode: 107
ASCII Unicode: 101
ASCII Unicode: 33
```

The `ord()` function allow us to see a single character’s decimal value from the ASCII table. Our python interpreter will consider this value to help compare strings.

To do the reverse of `ord()`, we can use the built-in `chr()` function to determine the character from a ASCII unicode.

```python
# Determining the character of a ASCII unicode

print('What is 42?', chr(42))
```

```
What is 42? *
```

#### Strings are Immutable <a href="#strings-are-immutable" id="strings-are-immutable"></a>

**Immutability**: The data type’s value cannot be altered without recreation of the value stored in a variable.

A single character or multiple characters cannot be changed in a string without redeclaring, recreating, or updating the variable with the intended change.

_Integers, Floating Points, Booleans, and Strings_ are considered to be Immutable Data types.

**Example:** Examine the error

```python
# Immutablity of String

name = 'Jim'
name[0] = 'T' # trying to change the first character of name: Jim to Tim

print(name)
```

```
---------------------------------------------------------------------------

TypeError                                 Traceback (most recent call last)

<ipython-input-6-3c0ceba28a1c> in <module>
      2
      3 name = 'Jim'
----> 4 name[0] = 'T' # trying to change the first character of name: Jim to Tim
      5
      6 print(name)


TypeError: 'str' object does not support item assignment
```
