# Commenting & Variables

<figure><img src="../../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

## What is a comment?

A comment is a way to leave notes for anyone who reads the code.

In JavaScript, the pattern `//` is reserved to create a single line of code that will be converted to a comment.

The JavaScript compiler will always ignore a line of comment when it sees the pattern of `//` in the beginning of the line.

## How does a JavaScript program execute its code?

The JavaScript compiler which translate our written instruction to a language that a computer can understand will translate the JavaScript code in order from top to bottom.

The code will then execute its instruction from top to bottom.

## What is a variable?

Variables are named placeholders that allow a programmer to attach important data that a program would need to an easy label that can be used to reference later.

### Variable Naming Convention

1. start with lowercase letters
2. labels that have multiple words are either `camelCased` or use `under_scores`
3. labels cannot be the same as the [built-in keywords](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/_keywords.html) in Java
4. labels should not be ambiguous `let a = "Park";` is less descriptive than `let last_name = "Park";`

## Our Program Above

```javascript
// Learning comments and variable
let greeting = "Hi, how are you?";

console.log(greeting);
```

1.  **Comment**:

    ```javascript
    // Learning comments and variable
    ```



    * This is a single-line comment. Comments are used to leave notes or explanations in your code. They are ignored by the JavaScript engine and do not affect the execution of the program.
2.  **Variable Declaration and Initialization**:

    ```javascript
    let greeting = "Hi, how are you?";
    ```



    * `let` is a keyword used to declare a variable. In this case, the variable is named `greeting`.
    * The variable `greeting` is assigned the string value `"Hi, how are you?"`.
3.  **Output to Console**:

    ```javascript
    console.log(greeting);
    ```



    * `console.log()` is a function that prints the value of `greeting` to the console.
    * When this line is executed, it will output: `Hi, how are you?`

So, when you run this program, it will display the message `"Hi, how are you?"` in the console.&#x20;

## Variable Creation and Variable Updates

```javascript
// This is a variable creation
let pet_name = "Marshall";
```

**Note:** You cannot create the same variable twice.

```javascript
// This is a variable creation done twice, which would cause an error
let pet_name = "Marshall";
let pet_name = "Freya";
```

If you wanted to change/update the value stored in a variable, you can just do a variable update.

```javascript
// This is a variable creation done twice, which would cause an error
let pet_name = "Marshall";
pet_name = "Freya";
```

You are allowed to re-reference a variable created and assign a new value when switching its value.

**WARNING:** the program will not remember its previous value.

## Recommended Readings

* Variables ([Link](https://javascript.info/variables))

