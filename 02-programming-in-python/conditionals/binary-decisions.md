# Binary Decisions

## `if` and `else` statements <a href="#if-and-else-statements" id="if-and-else-statements"></a>

```python

if (boolean condition):
    # if's code block

    code here
else:
    # else's code block

# end of the conditionals

code continues here
```

* The if’s code block only execute if its boolean condition is True
* The else’s code block will execute only when the if’s boolean condition is False
* This helps us create two pathways in our code

```python
# Code Example 1

num = 100

if num < 0 and num > 100:
    print(num, 'is invalid.')
else:
    print(num)

# since the if statement's condition is False we get to execute just the print(num) statement
```

```
Output:
100
```

```python
# Code Example 2

word = 'hello world!'

if 'o' in word:
    print('The letter o exists.')
else:
    print('The letter o does not exist.')

# examine that the print statement inside the else statement does not execute.
```

```
Output:
The letter o exists.
```
