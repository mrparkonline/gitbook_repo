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

## Converting data types of a variable

The act of changing the data type of a value is called **type casting.**

To examine the importance of this. We will look at the following code:

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

```javascript
// Screenshot's code:
let num1 = prompt("Enter number 1: ");
let num2 = prompt("Enter number 2: ");

console.log(num1 + num2);
```

The code is doing the following:

* created two variables and made them hold the results of the `prompt()` function
* we asked `console.log()` to output the addition of num1 and num2
* The output was 102 instead of our expected value fo 12 ...

_This occurred because the data type of variables in JavaScript is dynamic._&#x20;

When you create a variable in JavaScript, it will try to guess what type of data type it should be.&#x20;

However, the variable will not know what it is supposed to be at times when we say that a variable will contain the result of the `prompt()` function because we are not really given the context of the value that will be inputted.

## Typecasting Functions

### `Number()` a function to turn its arguments to numbers

In our previous code, we can update it to the following to make our `num1` and `num2` variables behave like numbers.

```javascript
let num1 = prompt("Enter number 1: ");
let num2 = prompt("Enter number 2: ");

num1 = Number(num1);
num2 = Number(num2);

console.log(num1 + num2); 
// the program will not output 12 instead of 102. if num1 is 10 and num2 is 2
```

### `String()` a function that turns its argument to strings

```javascript
let num = 123;
let digits = String(num); // digits is now "123"
```

There are time when you would want to convert a variable to a string if you need certain features that come with String objects.

## Related Readings

* Type Conversions ([Link](https://javascript.info/type-conversions))

