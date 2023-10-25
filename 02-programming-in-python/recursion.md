# Recursion

## What is Recursion?

Recursion is a programming and mathematical concept where a function or a process calls itself as a subroutine or part of its own execution. In other words, it's a technique where a problem is solved by breaking it down into smaller instances of the same problem.

{% hint style="info" %}
**TL;DR:** A function that calls itself again and again until we hit a base case

Recursion → _“defining something in terms of itself”_
{% endhint %}

### Recursion Recipe

All recursive algorithms must have the following:

1.  **Base Case:**

    Defining when the recursion should stop
2.  **Work toward Base Case:**

    How does our problem approach the base case?
3.  **Recursive Call:**

    Call the function again with a smaller instance which is actively working towards the basecase.

In a recursive algorithm, the computer "remembers" every previous state of the problem. This information is "held" by the computer on the "activation stack" (i.e., inside of each functions workspace).

Every function has its own workspace PER CALL of the function.

### How does Recursion solve problems?

**Let P be a problem:**

* Divide P into two or more subproblems (smaller instances)
* Divide until the subproblems are simple enough to be solved
* All the subproblem solutions are then combined to give a solution to the original problem

This is a basic program solving approach called: **“**[**Divide and Conquer Algorithm**](https://en.wikipedia.org/wiki/Divide-and-conquer\_algorithm)**”.**

This also leads to the basis of **“**[**Dynamic Programming**](https://en.wikipedia.org/wiki/Dynamic\_programming)**”.**

### Developing a Base Case

The base case should hold the simplest solution for the simplest, smallest instance of the problem

**Base Case:** In a recursion algorithm, the problem is broken down to subproblem until we reach the base case

{% hint style="info" %}
_Recursion algorithms are allowed to have multiple base cases._
{% endhint %}

Base cases are considered **“end conditions”**

## Types of Recursions

{% tabs %}
{% tab title="Single vs Multiple" %}
**Single** → It only calls itself once … only invokes one recursion to occur

* (Example: Adding up all numbers in a list)

**Multiple** → It can invoke multiple recursion to solve the answer

* (Example: Fibonacci → Fib(n) = Fib(n-2) + Fib(n-1)

The primary difference between single recursion and multiple recursion is the number of times a function invokes itself.&#x20;

Single recursion involves one recursive call, while multiple recursion involves multiple recursive calls within a single function. The choice between single and multiple recursion depends on the specific problem being solved and the problem's inherent structure.
{% endtab %}

{% tab title="Direct vs. Indirect Recursion" %}
Let `f` and `g` be functions.

Direct → `f` only calls `f`

Indirect → `f` calls `g` in which `g` calls `f` (can create longer chains)

* Indirect recursion can be also referred to as “_mutual recursions_”

The key difference between direct and indirect recursion is in how functions call each other.&#x20;

Direct recursion involves a function calling itself directly, while indirect recursion involves a group of functions that call each other in a cyclical manner to achieve a recursive result. The choice between direct and indirect recursion depends on the problem's structure and the relationships between functions in the program.
{% endtab %}
{% endtabs %}

## Code Examples

### Sum of All Numbers Below N.

{% tabs %}
{% tab title="Code" %}
```python
# Sum of All Numbers Below N --> Single Direct Recursion

def recursive_sum(num):
    # Base Case 
    if num == 0:
        return 0
    else:
        # Working towards the base case
        return num + recursive_sum(num)
```
{% endtab %}

{% tab title="Explanation" %}
**Base Case:**

* `N of 0` → No addition needed, we can return 0
* `N of 1` → No addition needed, we can return 1

**For all other N:**

* The sum of all numbers below `N` is `N + the recursive_sum of N-1`
{% endtab %}
{% endtabs %}

### Nth Fibonacci Number Generation

{% tabs %}
{% tab title="Code" %}
```python
# Nth Fibonacci Number --> Multiple Direct Recursion

def fib(n):
    if n == 0: # Base Case 1
        return 0
    elif n == 1: # Base Case 2
        return 1
    else:
        # Working towards two base cases.
        return fib(n-1) + fib(n-2)
```
{% endtab %}

{% tab title="Explanation" %}
1. `fib(n)` is called with an integer `n` as its argument.
2. The function checks for two base cases:
   * If `n` is 0, it returns 0. This is the base case for n = 0 in the Fibonacci sequence.
   * If `n` is 1, it returns 1. This is the base case for n = 1 in the Fibonacci sequence.
3. If `n` is neither 0 nor 1, the function proceeds to the recursive case:
   * It calculates `fib(n-1)` and `fib(n-2)` by making recursive calls to `fib` with the arguments `n-1` and `n-2`, respectively.
   * The recursive calls are working towards the base cases, essentially breaking down the problem into smaller subproblems.
   * The final result is obtained by summing the results of the recursive calls: `fib(n-1) + fib(n-2)`.
   * This step effectively constructs the Fibonacci sequence by recursively summing the two previous numbers in the sequence to find the nth Fibonacci number.
{% endtab %}
{% endtabs %}

## Recursion Optimization: Tail-Recursion

Tail recursion is a special form of recursion where the recursive call is the last operation performed in the function, allowing Python to optimize it by reusing the current function's stack frame.

1. **Define a base case:** As with any recursive function, start by defining the base case(s) that determine when the recursion should stop.
2. **Pass accumulated values as arguments:** Instead of relying on the call stack to maintain the state between recursive calls, pass the accumulated values as arguments to the recursive function. This ensures that the recursive call is the last operation in the function.
3. **Update arguments in the tail-recursive call:** In each recursive call, update the arguments to move towards the base case or the desired result. Continue to make the recursive call with these updated arguments until you reach the base case.

### Non-tail Recursive Factorial Function

```python
# Factorial Done Recursively

def r_factorial1(num):
    if num in {0,1}:
        return 1
    else:
        return num * r_factorial1(num-1)
```

### Tail Recursion Factorial Function

```python
# Factorial using Tail Recursion

def r_factorial2(num, tail=1):
    if num in {0, 1}:
        return tail
    else:
        return r_factorial(num-1, tail * num)
```

