# ⏮️ Iterations

An iteration refers to the repetition of a set of instructions or a block of code within a program. It is a fundamental concept used to execute a specific task or process multiple times until a certain condition is met or for a predetermined number of times.&#x20;

Iterations are typically achieved through constructs like loops (e.g., for loops, while loops) and are essential for automating repetitive tasks, processing collections of data, and solving problems that involve sequential or repetitive operations.&#x20;

Iterative algorithms play a crucial role in software development, enabling efficient and scalable solutions in various applications, from data processing and algorithm design to simulations and iterative optimization techniques.

## Types in Iterations in Python

* **While Loop** --> A condition-based iteration
* **For Loop** --> An iteration technique that traverses through [**iterable objects**](#user-content-fn-1)[^1]
* **Recursion** --> a programming technique where a function calls itself to solve a problem by breaking it down into smaller instances of the same problem.

## Using Iterations in Programming

### Rules & Mindset

1. Any iteration problem can be solved with a while loop, but not all for loops can solve while loop based solution.\
   \
   &#xNAN;_&#x41; while loop can have a complex condition that a for loop can't mimic._\
   \
   _A while loop can technically go on infinitely while its condition is true, but a for loop is almost always a finite loop._\

2. A for loop in Python is often considered to be more efficient in terms of performance compared to a while loop.\
   \
   &#xNAN;_&#x54;heir performance is similar and also dependent on the code block, but a for loop does not need to check a condition after each iteration to determine if they need to execute their code block._\
   \
   _Most often for loops are used in scenarios where the programmer knows the number of times they will iterate._\

3. Nesting a loop more than two or three levels are to be avoided.\
   \
   &#xNAN;_&#x53;ome solutions and algorithms cannot avoid going deeper than 3 levels due to its complexity. However, it is a good practice to not write solution that goes beyond 2 or 3 levels of nesting._

[^1]: In Python, iterable objects are data structures that can be looped over or iterated through to access their elements one at a time.
