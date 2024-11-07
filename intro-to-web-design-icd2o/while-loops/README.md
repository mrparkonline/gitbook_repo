# While Loops

A `while` loop in JavaScript allows you to execute a block of code repeatedly as long as a specified condition is `true`.

## How to write a while loop in JavaScript

```javascript
while (condition) {
  // code block to be executed
}
```

### Example

```javascript
let i = 0;

while (i < 10) {
  console.log("The number is " + i);
  i++;
}
console.log("The program is finished");
```

* A variable `i` has been set to 0.
* The while loop's condition is `i < 10`
  * As long as the loop's condition is evaluated to `true` it will repeat its code block
* The code block will do the following:
  * Output `The number is {i}` depending on the value of `i`
  * Increase `i` by one.
* The while loop will recheck its condition to see if it is `true` or `false`
  * if `true`, it will execute its code block
  * if `false`, it will move on with the rest of the code

#### Key Points

* **Condition Check**: The condition is evaluated before each iteration. If the condition is false initially, the loop body will not execute at all.
* **Use Cases**: `while` loops are useful when the number of iterations is not known beforehand and depends on some dynamic condition.
