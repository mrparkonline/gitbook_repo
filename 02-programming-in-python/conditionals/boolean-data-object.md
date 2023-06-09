# Boolean Data Object

Boolean is named after Mathematician [George Boole](https://en.wikipedia.org/wiki/George\_Boole).

The Boolean data type allow us to implement logic in our code by simplifying statements to be either True or False.

There are two Boolean data-typed possible values in Python.

* `True`
* `False`

**Usage:**

* We can set variables with Boolean values
* We can get them as a result from [Comparison, Logical, and Membership operations](comparison-logical-and-membership-operators.md)
* Certain functions and methods will result in a Boolean value as well

#### Truthy and Falsy Values in Python 3 <a href="#truthy-and-falsy-values-in-python-3" id="truthy-and-falsy-values-in-python-3"></a>

In programming (Python), certain values can be also True or False in Conditional Situations. We call these **Truthy** or **Falsy values**.

The rules are as follows:

* Idea of Emptiness is `False` → Keyword: `None` is `False`
* Therefore, `0, '', "" , []` are all empty → False
* 1 represents “ON” in binary → `True`; 0 → `False`
* Lastly, **ANY NON-FALSY** values are True

#### Type Conversion Function: `bool()` <a href="#type-conversion-function-bool" id="type-conversion-function-bool"></a>

The built-in function to convert one data value to Boolean is: `bool()`

```python
# Example

print('bool(\'\'):', bool('')) # Empty String
print('bool("Hello"):', bool("Hello")) # Non-Empty String
print('bool([]):', bool([]))
print('bool(1):', bool(1))
print('bool(0):', bool(0))

'''
bool(''): False
bool("Hello"): True
bool([]): False
bool(1): True
bool(0): False
'''
```
