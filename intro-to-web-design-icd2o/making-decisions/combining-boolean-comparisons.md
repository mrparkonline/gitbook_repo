# Combining Boolean Comparisons

In JavaScript, logical operators are used to perform logical operations on Boolean values (true or false) and are crucial in making decisions and controlling the flow of programs. The main logical operators are:

## **AND (`&&`)**

* Returns `true` if **both** operands are `true`.
* Returns `false` if **at least one** operand is `false`.

Example:

```javascript
let a = true;
let b = false;
console.log(a && b); // Output: false
```

## **OR (`||`)**

* Returns `true` if **at least one** of the operands is `true`.
* Returns `false` only if **both** operands are `false`.

Example:

```javascript
let a = true;
let b = false;
console.log(a || b); // Output: true
```

## **NOT (`!`)**

* Inverts the Boolean value of its operand.
* If the operand is `true`, it returns `false`; if the operand is `false`, it returns `true`.

Example:

```javascript
let a = true;
console.log(!a); // Output: false
```

## **Short-Circuiting Behavior**

* **AND (`&&`)**: If the first operand is `false`, JavaScript doesn’t evaluate the second operand because the entire expression will be `false`.
* **OR (`||`)**: If the first operand is `true`, JavaScript doesn’t evaluate the second operand because the entire expression will be `true`.

**Example:**

```javascript
let a = false;
let b = true;
console.log(a && b); // Output: false (b is not evaluated)
console.log(a || b); // Output: true (b is evaluated)
```

These operators are used in conditions, loops, and functions to make the code more dynamic by allowing complex conditions and logical flow.
