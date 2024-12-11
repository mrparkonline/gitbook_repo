# String Formatting

When we use `console.log()` or use Strings in our code, we can embed/inject values into a String without doing String manipulation.

```javascript
// String Formatting Example

let name = "Mr. Park";
let age = 32;
let message = `Hello, my name is ${name}, and I am ${age} years old.`;
console.log(message);
```

```
// Output:
Hello, my name is Mr. Park, and I am 32 years old.
```

Notice that the `message` variable has symbols such as `$, {, }`; however, the output of our program did not include such symbols.

This is because we used JavaScript's String formatting operation called Template Literals.

Template literals allow for string interpolation and are enclosed in backticks (`` ` ``) instead of single or double quotes. You can embed variables within the string using the `${}` syntax.

The `` ` `` key is found usually near the `1` key of your keyboard. It is not a single quotation mark.
