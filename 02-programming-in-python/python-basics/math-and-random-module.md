# Math & Random Module

## Math Module

The `math` module in Python is a built-in module that provides a set of mathematical operations and functions. It contains a wide range of mathematical functions, constants, and methods for performing various mathematical calculations.&#x20;

To use the `math` module, you need to import it into your Python script or interactive session using the `import` statement.

Here are some of the commonly used features of the `math` module:

1. **Mathematical Constants**: The `math` module provides constants such as `pi`, which represents the mathematical constant pi (approximately 3.14159), and `e`, which represents the mathematical constant e (approximately 2.71828).

```python
import math

print(math.pi)  # Output: 3.141592653589793
print(math.e)   # Output: 2.718281828459045
```

2. **Basic Mathematical Functions**: The module includes functions for performing basic mathematical operations like rounding, logarithms, exponentiation, square roots, trigonometric functions, and more.

```python
import math

print(math.sqrt(16))        # Output: 4.0
print(math.log10(1000))     # Output: 3.0
print(math.sin(math.pi/2))  # Output: 1.0
```

3. **Advanced Mathematical Functions**: The `math` module provides functions for advanced mathematical operations, such as factorials, absolute values, rounding, permutations, combinations, hyperbolic functions, and more.

```python
import math

print(math.factorial(5))       # Output: 120
print(math.fabs(-3.14))        # Output: 3.14
print(math.perm(5, 2))         # Output: 20
print(math.comb(5, 2))         # Output: 10
print(math.sinh(1.5))          # Output: 2.1292794550948173
```

4. **Numeric Operations**: The `math` module also includes functions for manipulating and working with numeric values, such as getting the floor and ceiling values, converting between radians and degrees, and checking for NaN (not a number) or infinity.

```python
import math

print(math.floor(3.7))    # Output: 3
print(math.ceil(3.2))     # Output: 4
print(math.radians(180))  # Output: 3.141592653589793
print(math.isnan(10))     # Output: False
print(math.isinf(float('inf')))  # Output: True
```

## Random Module

The `random` module in Python is a built-in module that provides functions for generating random numbers, selecting random elements from sequences, shuffling sequences randomly, and more. It is commonly used in scenarios that require randomness, such as simulations, games, and statistical analysis.&#x20;

To use the `random` module, you need to import it into your Python script or interactive session using the `import` statement.

Here are some commonly used features of the `random` module:

1. **Generating Random Numbers**: The `random` module provides functions to generate random numbers. The `random()` function returns a random float between 0 and 1.

```python
import random

random_number = random.random()
print(random_number)  # Output: a random float between 0 and 1
```

2. **Generating Random Integers**: The `random` module includes functions for generating random integers within a specified range.&#x20;

The `randrange()` function returns a random integer between the specified start and end values (inclusive). It also has an optional third argument called _step._ It determines the intervals between each number in the sequence.

```python
import random

random_integer = random.randrange(1, 10)
print(random_integer)  # Output: a random integer between 1 and 10 (exclusive of 10)
```

3. **Selecting Random Elements**: The `random` module allows you to select random elements from a sequence using the `choice()` function. It takes a sequence as an argument and returns a randomly selected element.

```python
import random

my_list = [1, 2, 3, 4, 5]
random_element = random.choice(my_list)
print(random_element)  # Output: a random element from the list
```

4. **Shuffling a Sequence**: The `random` module provides the `shuffle()` function to shuffle the elements of a sequence randomly. It modifies the original sequence in place.

```python
import random

my_list = [1, 2, 3, 4, 5]
random.shuffle(my_list)
print(my_list)  # Output: the original list with elements shuffled randomly
```

5. **Seeding the Random Number Generator**: The `random` module allows you to set a seed value using the `seed()` function. Setting a seed value ensures that the sequence of random numbers generated will be the same each time you run the program with the same seed value.

<pre class="language-python"><code class="lang-python"><strong>import random
</strong>
random.seed(42)
random_number = random.random()
print(random_number)  # Output: a deterministic random number based on the seed
</code></pre>

These are some of the commonly used features of the `random` module in Python. The `random` module provides a wide range of functions for generating randomness, selecting random elements, shuffling sequences, and more. It is a valuable tool for various applications that require randomness and randomization.
