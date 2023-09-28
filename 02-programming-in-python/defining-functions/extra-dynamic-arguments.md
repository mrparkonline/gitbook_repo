# \[Extra] Dynamic Arguments

In Python, `*args` and `**kwargs` are special features that provide flexibility when defining functions.&#x20;

`*args`, short for "arguments," allows a function to accept a variable number of non-keyword arguments. This means you can pass any number of positional arguments to the function, and they will be collected into a tuple within the function. This is particularly useful when you want to create functions that can handle an arbitrary number of input values.&#x20;

On the other hand, `**kwargs`, which stands for "keyword arguments," enables a function to accept a variable number of keyword arguments, which are collected into a dictionary within the function. This feature is handy when you want to work with named parameters and their values dynamically.&#x20;

## Using `*args` in your Function

`*args` is used to pass a variable number of non-keyword arguments to a function.&#x20;

It allows you to call a function with any number of positional arguments, which are then collected into a tuple.&#x20;

### Example: Sum of Numbers

```python
def sum_numbers(*args):
    result = 0
    for num in args:
        result += num
    return result

# Calling the function with different numbers of arguments
print(sum_numbers(1, 2, 3))  # Output: 6
print(sum_numbers(10, 20, 30, 40))  # Output: 100
print(sum_numbers(5))  # Output: 5
```

In this example, the `sum_numbers` function takes `*args` as its parameter. When you call the function, you can pass any number of arguments separated by commas. Inside the function, the arguments are collected into a tuple called `args`, and you can iterate through this tuple to perform operations, such as adding the numbers together in this case.

The key point here is that `*args` allows you to handle a variable number of arguments without having to specify each one individually in the function definition. It makes your code more flexible and adaptable to different input scenarios.

## Using `**kwargs` in your Functions

`**kwargs` (short for "keyword arguments") is used to pass a variable number of keyword arguments to a function.&#x20;

It allows you to call a function with any number of keyword arguments, which are then collected into a dictionary.&#x20;

### Example: A function that can display various dictionary combinations

```python
def display_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

# Calling the function with different keyword arguments
display_info(name="Alice", age=30)
display_info(name="Bob", occupation="Engineer", city="New York")
```

In this example, the `display_info` function takes `**kwargs` as its parameter. When you call the function, you can pass any number of keyword arguments in the form of `key=value` pairs. Inside the function, these keyword arguments are collected into a dictionary called `kwargs`. You can then iterate through this dictionary to access and display the key-value pairs.

Here's the output for the above example:

```
name: Alice
age: 30
name: Bob
occupation: Engineer
city: New York
```

The key benefit of `**kwargs` is that it allows you to handle a variable number of keyword arguments without having to specify each one individually in the function definition. This makes your code more flexible and adaptable, particularly when you want to work with functions that can accept different sets of named parameters.

Together, `*args` and `**kwargs` empower you to write more versatile and reusable functions that can adapt to different situations and data structures, making your Python code more robust and expressive.
