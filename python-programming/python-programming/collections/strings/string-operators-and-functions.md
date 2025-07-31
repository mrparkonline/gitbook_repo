# String Operators & Functions

#### String Operators <a href="#string-operators" id="string-operators"></a>

Much like how integers and floating point values have arithmetic operators, Strings also have built-in operators as well.

`+` Operator: **Concatenation**

* Concatenation is the joining of two string values

`*` Operator: **Repetition**

* Repetition operator allows us to repeat a certain string multiple times

`[start:end:step]` Operation: **Indexing** and **Slicing**

* With indexing and slicing, we can grab different parts of a given string

`in || not in` Operator: **Membership**

* We can check if a the left operand exists or does not exist in the right operand

**Examples:**

```python
# String Operation Examples

word1 = 'Hello, '
word2 = 'World!'

print('word1 + word2:', word1 + word2) # Concatenation

word3 = word1[:-2] # Slicing, resulting slice assigned to variable: word3
print('word3*3:', word3*3) # Repetition

print("'H' in word1:",'H' in word1) # Membership
print("'or' not in word2:", 'or' not in word2)

```

```
word1 + word2: Hello, World!
word3*3: HelloHelloHello
'H' in word1: True
'or' not in word2: False
```

#### Built-in Functions with Strings <a href="#built-in-functions-with-strings" id="built-in-functions-with-strings"></a>

**Using `max()` and `min()`**

* If given a single string argument, it will return a single character that has the greatest or the least ASCII value respectively
* If given multiple string arguments, they will compare each string’s characters in order and return the entire string that has the greatest or the least ASCII value respectively

_Example:_

```python
# Using max() and min() on strings

print("min('HelloWorld!'):", min('HelloWorld!'))
print("max('Hello', 'Goodbye!', 'World!'):", max('Hello', 'Goodbye!', 'World!'))
```

```
min('HelloWorld!'): !
max('Hello', 'Goodbye!', 'World!'): World!
```

**Using `len()`**

* Given a single string parameter, it will count how many alphanumeric and special characters there are as a positive integer

_Example:_

```python
# Using len() on a string

print("len('Hello, World!'):", len('Hello, World!'))
print("len(''):", len('')) # Empty String
print("len(' '):", len(' ')) # Single whitespace
print(type(''))
```

```
len('Hello, World!'): 13
len(''): 0
len(' '): 1
<class 'str'>
```

**Basic Type & Type Conversion Related Functions** `str()` function is used to convert a given argument into a string

* Anything from the standard python library can be converted to a string

`type()` function returns `<class 'str'>` on string values indicating that the given argument is a string value

`int()` function converts a numeric string to an integer

* the string argument must be able to turn into an integer
* converting a string-based decimal to an integer will result in error
* _Example:_ `int('42')` is 42, `int('3.14')` is an error

`float()` function converts a decimal-like string to a floating point

* if the numeric string has no decimal point, it will add a decimal point of .0
* _Example:_ `float('3')` is 3.0, `float('3.14')` is 3.14

`bool()` function converts a string to a Boolean value

* Non-empty strings are `True`
* An Empty string are `False`
