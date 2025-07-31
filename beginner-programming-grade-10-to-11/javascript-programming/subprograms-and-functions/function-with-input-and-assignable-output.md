# Function with Input and Assignable Output

To create more complex programs, we can have our functions be dependent on its inputs and give the ability to have the output of its functions be assigned to variables.

## Example: 420 checker.

We are going to create a program that checks if our given number is 420.

The function will take a single parameter, we will call it: `num`

The function will output either `true` if the given parameter is 420, `false` otherwise

### Our Program:

```javascript
// Function Definitions
function is_420(num) {
    if (num == 420) {
        return true;
    } else {
        return false;
    }
}
// End of Function Definitions

// Our Main Section
let result1 = is_420(69);
let result2 = is_420(420);

console.log(`Checking 69: ${result1}`);
console.log(`Checking 420: ${result2}`};
```

**Outputs:**

```
Checking 69: false
Checking 420: true
```

* **Function Declaration**: The function `is_420` is declared with one parameter `num`.
* **Parameter `num`**: This parameter will hold the value passed to the function when it is called. It is a placeholder variable to represent the potential values it can receive
  * As you can see, `num` was `69` in the first `console.log()` while being `420` in the second output.
* return is a keyword in JavaScript that has two important features:
* `return` allows us to assign a variable by creating a value from the function
* `return` also **ALLOWS THE FUNCTION TO ENDS ITS CODE EARLY** because the function will exit its code block when a `return` statement is executed
* In the example above:
  * **`if` Statement**: The function checks if `num` is equal to `420`.
    * **Condition `num == 420`**: If `num` is `420`, the function returns `true` and it is assigned to either variable `result1` or `result2` when the function is called
    * **`else` Statement**: If `num` is not `420`, the function returns `false` and it is assigned to either variable `result1` or `result2` when the function is called

```
Checking 69: false
Checking 420: true
```

* The following output above is possible because:
  * `result1` stores the result of `is_420()` with the given parameter of `69`
  * `result2` stores the result of `is_420()` with the given parameter of `420`
