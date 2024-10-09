# Creating Branches

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

## A Single Branch -> `if statement`

```javascript
let num = prompt("Enter a value");

if (num > 100) {
    console.log("Wow, that is a large number!");
}

console.log(`Your number is: ${num}`);
```

In this situation we created a single branch. The event that belongs to our if statement only executes if our given variable `num` is greater than 100.

Any code that belongs to a coding construct is called a `"code block"`

## Binary Branch -> `if ... else statement`

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

To create a program with two pathways where we can have an event occurs when our `if statement` evaluates to **false** is using an `else` statement.

```javascript
let num = prompt("Enter a value");

if (num > 100) {
    console.log("Wow, that is a large number!");
} else {
    console.log("Darn, that is a small number!");
}

console.log(`Your number is: ${num}`);
```

An `else` statement is not a requirement for all if clauses; however, you can use it if you want something to happen when the condition it is attached to is evaluated to `false`.
