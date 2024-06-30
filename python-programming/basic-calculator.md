# Basic Calculator

## Goal

Build a simple Python program that can add, subtract, multiply, and divide two numbers.

## Program Requirements

* Ability to obtain/read two numeric inputs from the user of the program
  * Store/remember the two inputs
* Do all the possible operations (add, subtract, multiply, divide) on the two numbers
* Display the output

### Extended Requirements

* Put restrictions on the inputs so that the inputted values from the user are numeric
* Ability to choose a desired operation (add, subtract, multiply, divide) from the user
  * Put restrictions on the denominator when dividing
* Execute the desired operation with the given inputs and store the result
* Output the stored results back to the user

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

#### Example Program Output

```
Enter number1: 5
Enter number2: 8

15 + 3 = 18
15 - 3 = 12
15 * 3 = 45
15 / 3 = 5
```
