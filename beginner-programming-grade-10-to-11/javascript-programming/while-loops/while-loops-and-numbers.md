# While Loops and Numbers

Calculations and Arithmetic are core component of programming. While loops can be used to ease the repetition and help us do complex calculations.

## Recipe to create generate numbers

1. Set a variable with the starting number
2. Set your condition to loop as long as it hasn't reached the final number to arrive at
3. Manipulate the variable at every loop as the last operation of the loop

{% hint style="info" %}
Recall that a while loop will always recheck its condition to see if it is `true` after its code block is done.
{% endhint %}

### Example

```javascript
let num = 1;

while (num < 10) {
    console.log(`Current number is: ${num}.`);
    
    num++;
}
```

**Initialization**: You start by setting a variable, `num` set to the value `1`.

**Condition Check**: You have a loop that will keep running as long as `num` is less than `10`.

**Loop Execution**: Inside the loop, you perform two main actions:

* Print the current value of `num` to the console.
* Increase the value of `num` by `1`.

**Repetition**: The loop checks the condition again. If `num` is still less than `10`, it repeats the actions inside the loop. This process continues, with `num` increasing by `1` each time, until `num` reaches `10`.

**Termination**: When `num` becomes `10`, the condition `num < 10` is no longer true, so the loop stops running.

In essence, this loop counts from `1` to `9`, printing each number along the way. The loop ensures that the actions inside it are repeated until a specific condition is no longer met.

### Example of going downwards

```javascript
let num = 100;

while (num > 0) {
    console.log(`Current number is: ${num}.`);
    
    num = num - 10;
}
```

**Initialization**: You start by setting a variable, which we’ll call `num`, to the value `100`.

**Condition Check**: You have a loop that will continue to run as long as `num` is greater than `0`.

**Loop Execution**: Inside the loop, two main actions occur:

* The current value of `num` is printed to the console.
* The value of `num` is decreased by `10`.

**Repetition**: After each iteration, the loop checks the condition again. If `num` is still greater than `0`, the loop repeats the actions. This process continues, with `num` decreasing by `10` each time, until `num` is no longer greater than `0`.

**Termination**: When `num` becomes `0` or less, the condition `num > 0` is no longer true, so the loop stops running.
