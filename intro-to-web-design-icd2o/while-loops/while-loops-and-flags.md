# While Loops and Flags

When writing programs that don't necessarily deal with numbers, you may use a flag based loop to help you do repetitions.

There are some problems that the end point of the task is unclear. In such scenario, it is helpful to write a potential infinite loop and construct an exit mechanism to get out of it.

## Example of a flag

_Please note that it does not need to be called a flag, but it is a representation of a flag being either being true or false._

```javascript
let flag = true;

while (flag) {
    console.log("Hello!");
    
    let end = prompt("Do you want to end the loop? (Yes/No): ");
    
    if (end == "Yes") {
        flag = false;
        console.log("good bye!");
    }
}
```

1. **Initialization**: You start by setting a variable called `flag` to `true`.
2. **Condition Check**: You have a loop that will continue to run as long as `flag` is `true`.
3. **Loop Execution**: Inside the loop, three main actions occur:
   * The message `“Hello!”` is printed to the console.
   * The program prompts the user with the question `“Do you want to end the loop? (Yes/No):”` and waits for the user’s input.
   * If the user types `“Yes”`, the `flag` variable is set to `false`, and the message `“good bye!”` is printed to the console.
4. **Repetition**: After each iteration, the loop checks the condition again. If `flag` is still `true`, the loop repeats the actions. This process continues until the user types `“Yes”` (case sensitive).
5. **Termination**: When the user types `“Yes”`, the condition `flag` becomes `false`, so the loop stops running, and the program prints `“good bye!”`.
