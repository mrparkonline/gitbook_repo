# Creating a Function in JavaScript

{% embed url="https://www.youtube.com/watch?v=Qki82Ns6tQs" %}



We have seen examples of built-in functions in JavaScript:

* `prompt()` allows us to grab user inputted values to assign to a variable
* `console.log()` is a method from the `console` that outputs text to the console

Similar to how these features have a `name`, ability to take `inputs`, and work with the inputs. We can create our own functions in JavaScript.

## Formatting a Custom Function in JavaScript

```javascript
function name_of_function(parameter1, parameter2) {
    // Function's code goes in here.
}
```

* The keyword `function` is used to let JavaScript know that we are creating a function
* `name_of_function` is used to name our custom function
* `(parameter1, parameter2)` is used to define any required inputs. They act as placeholders for the values that will be given to the function since the **`program cannot be certain of what the values will be.`**

### Example: A greeting function

```javascript
// Custom Functions Defined
function greet() {
    console.log("Hello, I am a program!");
}
// End of Custom Functions

// Start of our code
console.log("Welcome to our program!");
greet();
```

**Output:**

```
"Welcome to our program!"
"Hello, I am a program!"
```

* **Keyword `function`**: This keyword is used to declare a function.
* **Function Name `greet`**: This is the name of the function. You can call this function using this name.
* **Parentheses `()`**: These are used to define parameters for the function. In this case, there are no parameters.
* **Curly Braces `{}`**: These define the body of the function, which contains the code that will be executed when the function is called.
* **`console.log`**: This is a method of the `console` object that outputs a message to the web console.
* **String `"Hello, I am a program!"`**: This is the message that will be logged to the console.
* **When a function is defined, it is not executed until the function is called upon**
* The main instructions for the program starts under the comment: `// Start of our code`
  * The program will output first: `"Welcome to our program!"`
  * Then the program calls the function called `greet()`
  * The program then travels to the code block of `greet()` then executes the code to output `"Hello, I am a program!"`
