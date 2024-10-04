# Getting User Input

So far, we have created programs where we hardcoded the values for our variable.  We can make our program more interactive by implementing the ability to have the user input values to be stored in the variable by enter values in the console.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

If you notice the console (output) section, we **instructed** in our program to enter our name. When we provided a name and then press the enter key, we were able to assign `Park` to the variable `name`.

## The `prompt()` function

When the prompt() used in a normal HTML/CSS/JavaScript setting, it would open a pop up where you can enter a value.

In _Programiz,_ it will be a console based interaction to where you enter a value.

### How to use `prompt()`

* You must assign a variable to hold the value of `prompt()`
* Within the brackets, it is recommended that you write a string message to instruct the user on the console about what to input
  * The program will wait until the user of the program types their input into the console and pressed the `Enter` key
  * Once the `Enter` key is pressed, the program will continue with its instructions
* The data entered will be assigned to the variable

### Our code Example

```javascript
let name = prompt("Enter your name: ");
let message = `Hello, ${name}!`;

console.log(message);
```

The code written above uses the `prompt()` function to assign the value inputted by the user in the console.

The input will be assigned to the variable called `name`.

Depending on the value of `name`, The `console.log()` will output the message `"Hello, [NAME]!"`
