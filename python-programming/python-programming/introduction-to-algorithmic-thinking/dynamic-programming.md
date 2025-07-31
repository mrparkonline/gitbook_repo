# Dynamic Programming

**Dynamic programming** is similar to _Divide and Conquer_ method because it also breaks down its problem to simpler subproblems. The main difference is that it will store and memorize the calculations of subproblems to avoid redundant computations.

### Example: Adding numbers

_Recall that Divide and Conquer can effectively add numbers as well._

```
# Addition of numbers
6 + 5 + 3 + 3 + 2 + 4 + 6 + 5

# Breaking down to subproblems:
6 + 5, 3 + 3, 2 + 4, 6 + 5

There is a subproblem repeated --> 6 + 5
```

A divide and conquer algorithm would still compute 6 + 5.

A dynamic programming algorithm will remember that 6 + 5 has been solved, so it will just remember the result.

The term **`memoisation`** is the act of storing a solution to be used as a reference if a subproblem is encountered again.
