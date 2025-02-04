# If Statements

## If Statements <a href="#conditional-if-statements" id="conditional-if-statements"></a>

**Conditionals:** Features of programming language that allows different computations to occur based on decision making.

* Conditionals are dependent on Boolean expressions that are evaluated to **True** or **False**.
* Different texts will define conditionals to be statements, expressions, or constructs.
* The use of conditionals is the way to control the _flow_ of a program.

#### `if` statement <a href="#if-statement" id="if-statement"></a>

* `if` is a built-in keyword in Python that allows us to write conditional statements.
* if statements will only execute their own _block_ of code if its boolean condition evaluates to **True**.
* if the boolean condition doesn’t evaluate to True, the program will skip its _block_ of code
* Block of code or **Code Block** in python are started by a (:) colon and indentation. (Examine the example below)

```python
# if statement formatting template

if (boolean_expression_here): # notice the colon to start the if's code block
    # single indentation

    code written here
# end of the if statement

code written here ... outside of the if statement
```

```python
# Code Example 1
num1 = 10
num2 = 42
target = 34

if target >= num1 and target <= num2:
    print(target, 'is in between', num1, 'and', num2)
```

```
Output:
34 is in between 10 and 42
```

```python
# Code Example 2
word = 'Hello'

if len(word) >= 6:
    print(word, 'is too long.')

print(word)

# Notice that the message 'Hello is too long' is not outputted.
# This is because len(word) is less than 6 hence len(word) >= 6 is False
```

```
Output:
Hello
```
