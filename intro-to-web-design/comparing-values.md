# Comparing Values

Comparing values is a binary operation. We are comparing the values of the _left operand_ versus the _right operand._

## JavaScript's Comparison Operators

In JavaScript they are written like this:

* Greater/less than: `a > b`, `a < b`.
* Greater/less than or equals: `a >= b`, `a <= b`.
* Equals: `a == b`, please note the double equality sign `==` means the equality test, while a single one `a = b` means an assignment.
* Not equals: In math the notation is `≠`, but in JavaScript it’s written as `a != b`.

### Examples

```javascript
// Comparison Examples

let num1 = 42;
let num2 = 6;

console.log(`num1 == num2: ${num1 == num2}`);
console.log(`num1 != num2: ${num1 != num2}`);
console.log(`num1 > num2: ${num1 > num2}`);
console.log(`num1 < num2: ${num1 < num2}`);
console.log(`num1 >= num2: ${num1 >= num2}`);
console.log(`num1 <= num2: ${num1 <= num2}`);
```

```
Output:
num1 == num2: false
num1 != num2: true
num1 > num2: true
num1 < num2: false
num1 >= num2: true
num1 <= num2: false
```

_Comparison operation will result into a Boolean value_

## Recommended Readings

**Comparisons (**[**Link**](https://javascript.info/comparison)**)**
