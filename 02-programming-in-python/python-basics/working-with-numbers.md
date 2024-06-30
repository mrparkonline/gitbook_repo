# Working with Numbers

Due to the fast computational speeds of computers, programs are often written to do complex math.

Using the arithmetic operators in Python will automatically follow order of operations.

## Addition, Subtraction, Multiplication

```python
# Examples of Adding, Subtracting, and Multiplying Values

x = 10
y = 11
z = 12

print(x + y) #  21 will be printed
print(x - z) #  -2 will be printed
print(y * z) # 132 will be printed

result = (x * y) + z # the result variable will contain 122
```

## Division & Floor Division

```python
# Examples of using both division and floor division

x = 10
y = 15
z = 3

print(x / z) # prints a floating point value of 3.3333333
print(x // z) # prints an integer value of 3

result1 = (y / z) # result1 contains a floating point value of 5.0
result2 = (y // z) # result2 contains an integer value of 5
```

The division operation (`/`) in Python will enforce a floating point result.

The floor operation (`//`) in Python will enforce an integer result. It will also round down to the nearest integer always.

Both division operations will result in an error when trying to divide by zero.

## Modulus Operation

The modulus operation, denoted by the `%` symbol in Python calculates the remainder of the division between two numbers. It returns the remainder after dividing one number (the dividend) by another (the divisor).

For example, if you perform the modulus operation `x % y`, the result will be the remainder when `x` is divided by `y`.

```python
# Example of using the modulus operator

x = 10
y = 3

result = x % y
print(result)  # Output: 1
```

In this example, `x` is divided by `y`, which yields a quotient of `3` with a remainder of `1`. Therefore, the value of `result` will be `1`.

Modulus is often used in programming for various purposes:

1. **Checking divisibility:** By using the modulus operator, you can determine if a number is divisible by another number. If the result is `0`, it means the number is evenly divisible; otherwise, there is a remainder.
2. **Cycling and wrapping values:** Modulus is frequently used to wrap values within a specific range. For example, you might use `(x % n)` to ensure that `x` stays within the range of `0` to `(n-1)`.
3. **Generating sequences:** Modulus can be used to create patterns or sequences. By applying a modulus operation to an incrementing variable, you can create repetitive patterns or cycle through a fixed set of values.
