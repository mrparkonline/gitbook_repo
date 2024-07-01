# Improving the calculator

## Goal

The previous calculator can be considered a minimal viable product; therefore, it has some weaknesses. Our goal in this page is to analyze what can be done to improve it.

### Previous Python Code w/ Commentary

```python
# Basic Calculator
# Input Handling
number1 = int(input("Enter number 1: "))
number2 = int(input("Enter number 2: "))

# Since we convert the inputs to integers, we cannot handle inputs with decimals.
# There is no feature built-in to our to prevent non-numeric inputs at the moment.

# Operations
result1 = number1 + number2
result2 = number1 - number2
result3 = number1 * number2
result4 = number1 / number2

# Instead of asking the user which operation to perform, we execute all the operations.

# Output
print(f"{number1} + {number2} = {result1}")
print(f"{number1} - {number2} = {result2}")
print(f"{number1} * {number2} = {result3}")
print(f"{number1} / {number2} = {result4}")
```

### Extended Requirements

* Ability to choose a desired operation (add, subtract, multiply, divide) from the user
* Put restrictions on the inputs so that the inputted values from the user are numeric
* Allow the program to obtain decimal inputs.
* Put restrictions on the denominator when dividing; cannot be zero.
* Execute the desired operation with the given inputs and store the result
* Output the stored results back to the user

## User Chooses Desired Operation

```python
# User choosing a desired operation
print('''Please chooses the following possible operations:
- 1. Add
- 2. Subtract
- 3. Multiply
- 4. Divide
''')

choice = None
while True:
    choice = input("Option chosen: ")
    choice = choice.lower()
    
    if choice not in {'add', 'subtract', 'multiply', 'divide'}:
        print("Invalid option, please choose again.")
    else:
        print(f"Operation {choice} was chosen.")
        break
# end of desired operation handling
```

### Code 1 Explanation:

1. **Printing the Operation Choices:**

```python
print('''Please chooses the following possible operations:
- 1. Add
- 2. Subtract
- 3. Multiply
- 4. Divide
''')
```

This block of code uses a multi-line string (enclosed in triple single quotes) to print a list of possible operations the user can choose from.&#x20;

The operations are listed as `Add`, `Subtract`, `Multiply`, and `Divide`.

2. **Initializing the Choice Variable:**

```python
choice = None
```

This initializes the variable `choice` to `None`. This step is not strictly necessary since the variable is immediately assigned a value inside the `while` loop, but it can be useful for clarity and to avoid potential reference before assignment errors.

3. **Starting an Infinite Loop:**

```python
while True:
```

This begins an infinite loop, which will keep running until it is explicitly broken.

4. **Prompting the User for Input:**

```python
choice = input("Option chosen: ")
choice = choice.lower()
```

Inside the loop, the user is prompted to input their choice of operation. The `input` function captures this input as a string. The `choice.lower()` method converts the input to lowercase to ensure case-insensitivity when checking the user's input.

5. **Validating the User's Choice:**

```python
if choice not in {'add', 'subtract', 'multiply', 'divide'}:
    print("Invalid option, please choose again.")
else:
    print(f"Operation {choice} was chosen.")
    break  # Added break to exit the loop when a valid choice is made
```

The code checks if the user's input (`choice`) is one of the valid operations (`'add'`, `'subtract'`, `'multiply'`, `'divide'`).&#x20;

If the input is not valid, it prints an error message and the loop continues, prompting the user again.&#x20;

If the input is valid, it prints a confirmation message and breaks out of the loop, ending the infinite loop.

## Numeric Inputs Only + Supporting Decimals

```python
# Numeric Inputs Only
number1 = None
while True:
    try:
        user_input = input("Enter number 1:")
        number1 = float(user_input)
        print(f"First Input: {number1}")
        break
    except ValueError:
        print(f"{user_input} cannot be converted to a floating point value")        
```

### Code 2 Explanation:

1. **Variable Initialization:**

```python
codenumber1 = None
```

This initializes the variable `number1` to `None`. This variable will later store the user's input after it has been successfully converted to a float.

2. **Infinite Loop:**

```python
while True:
```

The `while True` loop runs indefinitely until it is explicitly broken. This allows the program to continually prompt the user for input until valid input is received.

3. **Try Block:**

```python
try:
    user_input = input("Enter number 1:")
    number1 = float(user_input)
    print(f"First Input: {number1}")
    break
```

* `user_input = input("Enter number 1:")`: This line prompts the user to enter a value and stores the input as a string in `user_input`.
* `number1 = float(user_input)`: This line attempts to convert the input string to a floating point number and assigns it to `number1`.
* `print(f"First Input: {number1}")`: If the conversion is successful, this line prints the successfully converted floating point number.
* `break`: If the conversion and print statements are successful, the `break` statement exits the infinite loop, indicating that valid input has been received.

4. **Except Block:**

```python
except ValueError:
    print(f"{user_input} cannot be converted to a floating point value")
```

* If the conversion `float(user_input)` raises a `ValueError` (meaning the input could not be converted to a float), the `except` block is executed.
* `print(f"{user_input} cannot be converted to a floating point value")`: This line prints an error message indicating that the input was invalid and could not be converted to a float.

{% hint style="info" %}
Code 2 seems to be useful in the future ... put it inside a function.
{% endhint %}

```python
# Numeric Input Code held in a function
def numericInput(prompt: str) -> float:
    number1 = None
    while True:
        try:
            user_input = input(prompt)
            number1 = float(user_input)
            print(f"First Input: {number1}")
            return number1 # instead of break
        except ValueError:
            print(f"{user_input} cannot be converted to a floating point value")
# end of numericInput()
```

## Restrict Division by Zero

_-- lets assume that variable: `choice = "divide"`_

```python
# Restrict Division by Zero

if choice == "divide":
    try:
        result = number1 / number2
    except ZeroDivisionError:
        result = None
        print(f"Since the variable number2 is a zero, there is no solution.")
```

1. **Conditional Check:**

```python
if choice == "divide":
```

This line checks if the user has chosen the division operation. If `choice` is equal to the string `"divide"`, the code inside the `if` block will be executed.

2. **Try Block:**

```python
try:
    result = number1 / number2
```

The `try` block attempts to perform the division `number1 / number2`.

If `number2` is not zero, the division is successful, and the result is assigned to the variable `result`.

3. **Except Block:**

```python
except ZeroDivisionError:
    result = None
    print(f"Since the variable number2 is a zero, there is no solution.")
```

If `number2` is zero, attempting to divide by zero raises a `ZeroDivisionError`.

The `except` block catches this exception.

Inside the `except` block, `result` is set to `None` to indicate that the division could not be performed.

A message is printed to inform the user that division by zero is not possible.

## The Full Final Code

```python
# Basic Calculator v2

# Numeric Input Code held in a function
def numericInput(prompt: str) -> float:
    number1 = None
    while True:
        try:
            user_input = input(prompt)
            number1 = float(user_input)
            print(f"First Input: {number1}")
            return number1 # instead of break
        except ValueError:
            print(f"{user_input} cannot be converted to a floating point value")
# end of numericInput()

# User choosing a desired operation
print('''Please chooses the following possible operations:
- 1. Add
- 2. Subtract
- 3. Multiply
- 4. Divide
''')

choice = None
while True:
    choice = input("Option chosen: ")
    choice = choice.lower()
    
    if choice not in {'add', 'subtract', 'multiply', 'divide'}:
        print("Invalid option, please choose again.")
    else:
        print(f"Operation {choice} was chosen.")
        break
# end of desired operation handling

# Using our custom numericInput Function
number1 = numericInput("Enter Number 1: ")
number2 = numericInput("Enter Number 2: ")

# Doing our desired calculation
result = None
if choice == "add":
    result = number1 + number2
elif choice == "subtract":
    result = number1 - number2
elif choice == "multiply":
    result = number1 * number2
elif choice == "divide":
    # Restrict Division by Zero
    if choice == "divide":
        try:
            result = number1 / number2
        except ZeroDivisionError:
            result = None
            print(f"Since the variable number2 is zero, there is no solution.")

# Outputting the result
if result is not None:
    print(f"The result is: {result}.")
```

### Code Explanation:

1. **Defining the Numeric Input Function**

```python
# Numeric Input Code held in a function
def numericInput(prompt: str) -> float:
    number1 = None
    while True:
        try:
            user_input = input(prompt)
            number1 = float(user_input)
            print(f"First Input: {number1}")
            return number1 # instead of break
        except ValueError:
            print(f"{user_input} cannot be converted to a floating point value")
# end of numericInput()
```

* `def numericInput(prompt: str) -> float:` defines a function named `numericInput` that takes a string `prompt` and returns a float.
* Inside the function, an infinite loop is used to repeatedly prompt the user for input until a valid float is provided.
* The `try...except` block attempts to convert the user's input to a float and returns it if successful. If not, it catches the `ValueError` and prompts the user again.

2. **User Choosing a Desired Operation**

```python
# User choosing a desired operation
print('''Please choose the following possible operations:
- 1. Add
- 2. Subtract
- 3. Multiply
- 4. Divide
''')

choice = None
while True:
    choice = input("Option chosen: ").lower()
    
    if choice not in {'add', 'subtract', 'multiply', 'divide'}:
        print("Invalid option, please choose again.")
    else:
        print(f"Operation {choice} was chosen.")
        break
# end of desired operation handling
```

* A multi-line string is printed to show the user the available operations.
* An infinite loop prompts the user to choose an operation.
* The user's input is converted to lowercase to ensure case-insensitive comparison.
* If the input is not a valid option, the user is prompted again. If it is valid, the loop breaks.

3. **Using the Numeric Input Function**

<pre class="language-python"><code class="lang-python"><strong># Using our custom numericInput Function
</strong>number1 = numericInput("Enter Number 1: ")
number2 = numericInput("Enter Number 2: ")
</code></pre>

**`numericInput()`:**

* The `numericInput()` function is called twice to get two numeric inputs from the user, storing them in `number1` and `number2`.

4. **Performing the Desired Calculation**

```python
# Doing our desired calculation
result = None
if choice == "add":
    result = number1 + number2
elif choice == "subtract":
    result = number1 - number2
elif choice == "multiply":
    result = number1 * number2
elif choice == "divide":
    # Restrict Division by Zero
    if choice == "divide":
        try:
            result = number1 / number2
        except ZeroDivisionError:
            result = None
            print(f"Since the variable number2 is a zero, there is no solution.")
```

**Performing the Operation:**

* Based on the user's choice, the appropriate arithmetic operation is performed.
* If the user chose "divide" -> a `try...except` block handles the possibility of division by zero.&#x20;
  * If `number2` is zero, a `ZeroDivisionError` is caught, and `result` is set to `None`.

4. **Outputting the Result**

```python
# Outputting the result
if result is not None:
    print(f"The result is: {result}.")
```

* If `result` is not `None`, it means the calculation was successful, and the result is printed.
* If `result` is `None`, it indicates an error occurred (e.g., division by zero), and no result is printed.

#### Key Points:

* **Input Validation:** The `numericInput` function ensures only valid numeric inputs are accepted.
* **Operation Selection:** A loop ensures the user selects a valid operation.
* **Error Handling:** Division by zero is handled gracefully using a `try...except` block.
* **Function Reusability:** The `numericInput` function is reusable for any numeric input prompt, making the code modular and clean.
