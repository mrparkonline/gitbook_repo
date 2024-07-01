# Basic Calculator

## Goal

Build a simple Python program that can add, subtract, multiply, and divide two numbers.

## Program Requirements

* Ability to obtain/read two numeric inputs from the user of the program
  * Store/remember the two inputs
* Do all the possible operations (add, subtract, multiply, divide) on the two numbers
* Display the output

## Pseudocode of the Calculator

{% hint style="info" %}
Pseudocode is a simplified, informal way of describing the steps and logic of a computer program or algorithm. It uses a mixture of natural language and basic programming structures to outline the flow of the program without being tied to the syntax of any specific programming language.
{% endhint %}

### Pseudocode 1: Basic Calculator

```
input NUMBER1
input NUMBER2

RESULT1 = NUMBER1 + NUMBER2
RESULT2 = NUMBER1 - NUMBER2
RESULT3 = NUMBER1 * NUMBER2
RESULT4 = NUMBER1 / NUMBER2

output RESULT1
output RESULT2
output RESULT3
output RESULT4
```

This program stores two inputs in two separate variables. Then it generates 4 more variables to store each of the resulting operation. Lastly, the program will output the stored operations to complete its execution.

A computer program is a set of instruction that a computer will follow to complete a given task; therefore, the computer will start from line 1 of the program, and it will execute all of the given instructions until the end of its instruction set.

### Python Translation

```python
# Basic Calculator
# Input Handling
number1 = int(input("Enter number 1: "))
number2 = int(input("Enter number 2: "))

# Operations
result1 = number1 + number2
result2 = number1 - number2
result3 = number1 * number2
result4 = number1 / number2

# Output
print(f"{number1} + {number2} = {result1}")
print(f"{number1} - {number2} = {result2}")
print(f"{number1} * {number2} = {result3}")
print(f"{number1} / {number2} = {result4}")
```

This Python program above is a direct translation of our program designed as a pseudocode.

* The `#` symbol is used to create comments; a way to leave readable notes for the reader, but an ignored line of code by the Python Interpreter.
* `input()` is a [built-in function](#user-content-fn-1)[^1] that reads a typed text within the console[^2].
* `int()` is a built-in function that converts a given argument[^3] into an integer.
* `print()` is a built-in function that outputs text-based data (called a [_String_](#user-content-fn-4)[^4]) to the console.

{% hint style="info" %}
Why do we apply `int()` function on our `input()` function?

The `input()` function will always read any data as a String-typed data. Therefore, we cannot treat the inputted value to invoke a numeric behavior (_aka apply arithmetic operations_). For the Python interpreter to properly understand how to use the given input, we must converted the inputs to integers for this situation.
{% endhint %}

Within our `print()` function, we are outputting formatted strings or "**f-strings**".

`f-strings` are special types of strings that allow the direct values of variables embedded via curly braces `{}` and it maintains the format of the strings based on how the data was defined.

#### Example Program Output

<pre><code><strong>[INPUT]
</strong><strong>Enter number1: 5
</strong>Enter number2: 8

[OUTPUT]
15 + 3 = 18
15 - 3 = 12
15 * 3 = 45
15 / 3 = 5
</code></pre>

### Connected Reading

_Connected reading is a section dedicated to provide fundamental knowledge to the important aspects introduced in this page._

* [ ] Definitions for Python ([link](https://mrparkonline.gitbook.io/guide-to-high-school-computer-science/ics4u1-content-2023/02-programming-in-python/python-basics))
* [ ] F-strings and String Formatting ([link](https://mrparkonline.gitbook.io/guide-to-high-school-computer-science/ics4u1-content-2023/02-programming-in-python/python-basics/string-formatting))
* [ ] Use of `int()` -> "Type Casting" ([link](https://mrparkonline.gitbook.io/guide-to-high-school-computer-science/ics4u1-content-2023/02-programming-in-python/python-basics/data-types#type-casting))
* [ ] Input & Output to the Console ([link](https://mrparkonline.gitbook.io/guide-to-high-school-computer-science/ics4u1-content-2023/02-programming-in-python/python-basics/input-and-output-to-console))
* [ ] Arithmetic Operators ([link](https://mrparkonline.gitbook.io/guide-to-high-school-computer-science/ics4u1-content-2023/02-programming-in-python/python-basics/working-with-numbers))

[^1]: A feature that comes with the given programming language

[^2]: The console refers to the interface where you interact with the Python interpreter

[^3]: An argument is data passed onto a function within the function's brackets so that the function can process the given data and generate/return a new result

[^4]: In Python, strings are immutable sequences of characters enclosed within single quotes (`'...'`), double quotes (`"..."`), triple single quotes (`'''...'''`), or triple double quotes (`"""..."""`).
