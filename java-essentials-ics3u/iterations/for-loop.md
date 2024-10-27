# For Loop

A for loop is an iteration that is designed to repeat its block of code a certain number of times.

```java
for (initialization; condition; update) {
    // Code to be executed repeatedly
}
```

1. **Initialization:** This part is used to initialize a loop control variable. It typically declares and initializes a counter variable before entering the loop.
2. **Condition:** This is a boolean expression that determines whether the loop should continue executing or terminate. If the condition evaluates to `true`, the loop continues; if it evaluates to `false`, the loop exits.
3. **Update:** This part is used to update the loop control variable after each iteration of the loop. It can be used to increment or decrement the counter variable.
4. **Code block:** The code block enclosed within curly braces `{}` is the body of the loop. It contains the statements that you want to execute repeatedly as long as the condition is true.

```java
// Example Code. Printing 1 to 5.
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

* `int i = 1` initializes the loop control variable `i` to 1.
* `i <= 5` is the condition. As long as `i` is less than or equal to 5, the loop will continue.
* `i++` is the update statement, which increments `i` by 1 after each iteration.

The loop will run for values of `i` from 1 to 5, printing each value, and then exit when `i` becomes 6 (because `6 <= 5` evaluates to `false`).
