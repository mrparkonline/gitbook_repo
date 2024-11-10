# Infinite While Loop

An **infinite while loop** is a loop that continues to execute indefinitely because the loop’s condition always evaluates to `true`.&#x20;

This can happen either intentionally or unintentionally, and it can cause a program to become unresponsive or crash if not handled properly.

## Example

```javascript
let num = 1;
while (num < 10) {
    console.log("This loop will run forever!");
}
```

In this example, the condition `num < 10` is always `true`, so the loop will never stop running. This is an example of an unintentional infinite loop.

{% hint style="info" %}
To avoid creating an infinite loop by mistake, make sure your loop’s condition will eventually become `false`.
{% endhint %}

Making sure our variable updates at every loop towards the `false` condition:

```javascript
let num = 1;
while (num < 10) {
    console.log("This loop will run forever!");
    num++;
}
```

## Use Case: Game Loops

Game loops are a classic example of infinite loops used in programming. They are essential for running the main logic of a game, continuously updating the game state, processing user input, and rendering graphics.
