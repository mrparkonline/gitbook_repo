# Subprograms & Functions

## Subprograms

A subprogram is a set of instructions designed to perform a specific task, which can be called and executed from different parts of a program.

### Functions

Functions are an example of subprograms.

* Functions are named containers of code that are designed to complete a very specific task
* As long as the function is defined prior to being used/called, the program will execute the code inside the function

### Two Benefits of Functions

1. Reusability

Programmers often write code that can be beneficial in future programs or in the future sections of the code. If we write that code within a function, we can prevent re-writing it by just `"calling"` the function after we define it.

2. Clean Code

Functions provide a way to organize and structure our code. By breaking down core components of the problem requirements within functions, it improves both readability and simplicity to testing our code.

## Structures of Functions in JavaScript

1. Define a function with its parameters, construct its code block, make end points if the function generates a returnable output
2. To use the created functions, we call it by its name followed by brackets, and we insert the required parameters if needed.
3. If the function generates a value, it can be assigned to a variable

## Definition Differences `functions` vs `methods`

* Functions are independent from a data type, they are standalone containers of code.
* Methods are features of a data type object, only certain data types will provide such features.

**Example**

1. `prompt()` is a function it is not tied to any data type.
2. `"Hello".at(2)` is an example of a method that is provided by the String data type.
