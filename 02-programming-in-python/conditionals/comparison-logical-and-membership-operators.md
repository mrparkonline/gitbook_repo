# Comparison, Logical, and Membership Operators

In this lesson, we will be talking about built-in Python operators that will give us a Boolean result.

#### Comparison Operators <a href="#comparison-operators" id="comparison-operators"></a>

Comparison operators help us compare the left and the right operand in terms of magnitude.

```
Symbols:
    == Equal to
    != Not Equal to
    > Greater than
    < Less than
    >= Greater than or Equal to
    <= Less than or Equal to
```

```python
# Comparison Examples

num1 = 42
num2 = 6

print('num1 == num2:', num1 == num2)
print('num1 != num2:', num1 != num2)
print('num1 > num2:', num1 > num2)
print('num1 < num2:', num1 < num2)
print('num1 >= num2:', num1 >= num2)
print('num1 <= num2:', num1 <= num2)
```

```
Output:
num1 == num2: False
num1 != num2: True
num1 > num2: True
num1 < num2: False
num1 >= num2: True
num1 <= num2: False
```

#### Logical Operators <a href="#logical-operators" id="logical-operators"></a>

We use logical operators to combine boolean expressions.

```
Keywords:
    and : both the left and the right side of [and] must evaluate to True for the entire statement to be True
    or : either one of or both the left right side of [or] must evaluate to True for the entire statement to be True
    not : turns a True to False, and False to True
```

The most basic boolean expressions possible are `True` and `False`.

```python
# Logical Examples

expr1 = True
expr2 = False

print('expr1 and expr2:', expr1 and expr2)
print('expr1 or expr2:', expr1 or expr2)
print('not(expr1):', not(expr1))
print('not expr2:', not expr2)
```

```
Output:
expr1 and expr2: False
expr1 or expr2: True
not(expr1): False
not expr2: True
```

#### Membership Operators <a href="#membership-operators" id="membership-operators"></a>

Membership operation allow us to check for the exitence of data from an iterable data type.

```
    Keywords:
    - in : Checks if the left operand exists in the right operand
    - not in : Checks if the left operand does not exist in the right operand
```

We will look at some examples with Strings and Lists.

```python
# Membership Example 1

letter1 = 'a'
letter2 = 'ell'
word = 'hello'

print('a in hello:', letter1 in word)
print('a not in hello:', letter1 not in word) # equivalent to print('not (a in hello)', not (letter1 in word))
print('----')
print('ell in hello:', letter2 in word)
print('ell not in hello:', letter2 not in word)
```

```
Output:
a in hello: False
a not in hello: True
----
ell in hello: True
ell not in hello: False
```

```python
# Membership Example 2

fruits = ['Oranges', 'Kiwis', 'Apples', 'Watermelons']

print('Strawberries in fruits:', 'Strawberries' in fruits)
print('kiwis in fruits:', 'Kiwis' in fruits)
```

```
Output:
Strawberries in fruits: False
kiwis in fruits: True
```

#### Order of Precedence/Operations in Python 3 <a href="#order-of-precedenceoperations-in-python-3" id="order-of-precedenceoperations-in-python-3"></a>

During assignment or boolean expression evaluation, the order of calculation follows:

```
    1. Anything in Parenthesis ()
    2. ** (Exponentiation)
    3. *, /, %, // (Multiply, Divide, Modulus, Floor Division)
    4. +, - (Addition, Subtraction)
    5. <=, <, >, >= (Comparison Operators)
    6. ==, != (Equality Operators)
    7. =, %=, /=, //=, -=, +=, *=, **=, (Assignment Operators)
    8. in, not in (Membership operators)
    9. not, or, and (Logical Operators)
```
