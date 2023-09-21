# Input & Output to Console

[**`input(__parameter__)`**](https://docs.python.org/3/library/functions.html#input) is a [built-in function](useful-built-in-functions.md) that is able to grab keyboard based input from the console.&#x20;

The `input()` function has an optional parameter which takes a single string. This string can be considered as a prompting message to help users identify what type of data to input.

[**`print(__parameter__)`**](https://docs.python.org/3/library/functions.html#print)  is a built-in function that helps to output a message to the console.

The `print()` function can take any number of parameters separated by commas. This will output such parameters separated by a whitespace into the console.

```python
# Fahrenheit to Celsius Converter

fahrenheit = input("Enter a fahrenheit value: ")
fahrenheit = float(fahrenheit)

celsius = (fahrenheit - 32.0) * (5/9)

print(fahrenheit, "is converted to:", celsius, "in celsius")
```

## **Code Explanation**

```python
fahrenheit = input("Enter a fahrenheit value: ")
fahrenheit = float(fahrenheit)
```

* The first line prompts the user to enter a Fahrenheit value.
* The input function is used to read the user's input, which is initially a string.
* The second line converts the input value from a string to a floating-point number using the `float()` function and assigns it to the variable `fahrenheit`.

```python
celsius = (fahrenheit - 32.0) * (5/9)
```

* The next line calculates the Celsius equivalent of the Fahrenheit value.
* The formula used is `(Fahrenheit - 32) * (5/9)` to convert Fahrenheit to Celsius.
* The result is assigned to the variable `celsius`.

```python
print(fahrenheit, "is converted to:", celsius, "in celsius")
```

* Finally, the last line displays the original Fahrenheit value entered by the user, along with the converted Celsius value.
* The `print()` function is used to output the values to the console.
* The values are separated by commas, which are automatically converted to strings and concatenated.
