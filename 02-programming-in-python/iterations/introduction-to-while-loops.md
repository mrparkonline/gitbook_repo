# Introduction to While Loops

**Iteration** is the act of repeating a mathematical or computational process. Each repeated step in iteration is also called an iteration.

## While Loops <a href="#while-loops" id="while-loops"></a>

While loops are our very first iteration statements that we can incorporate into our program. It behaves very similar to an if statement; however, a while loop will repeat its code block when its condition evaluates to True.

```python
# While Loop Format

while __boolean_condition__:

    your code here

# end of while loop
```

We can use while loops to complete repetitive tasks, generate ranges of values, and express algorithms.

When a while loop reaches the end of its code block, it will always re-evaluate its Boolean condition.

* If the condition is **`True`**, it will execute its code block again
* If the condition is **`False`**, it will ignore the code block and continue on with the flow of the program.

### Example: Printing Factors of a Number

{% tabs %}
{% tab title="Code" %}
```python
# Example Program 1:
# Factors of a Number

num = 12
divisor = 1

while divisor <= num:
    if num % divisor == 0:
        print(divisor, 'is a factor of', num)

    divisor += 1
# end of while
```
{% endtab %}

{% tab title="Output" %}
```
1 is a factor of 12
2 is a factor of 12
3 is a factor of 12
4 is a factor of 12
6 is a factor of 12
12 is a factor of 12
```
{% endtab %}
{% endtabs %}

**Code Explanation:**

* We only repeat the while loop’s code block if divisor is less or equal to num.
* During every iteration, we are checking a condition
  * If the condition is `True`, we output the factor
* To make sure we exit the loop eventually, we are modifying divisor variable so that the while loop’s condition will evaluate to `False`

## Python Specific: While … Else Structure <a href="#python-specific-while--else-structure" id="python-specific-while--else-structure"></a>

There is no **`elif`** for while loops, but we can add an `else` statement to make sure to _execute certain code block when the while loop’s condition evaluates to False._

{% tabs %}
{% tab title="Code" %}
```python
# Example 2: while loop's condition is False right at the beginning

num = 3

while num % 2 == 0:
    print(num)
    num //= 2
else:
    print('We have reached an odd number.')
```
{% endtab %}

{% tab title="Output" %}
```
We have reached an odd number.
```
{% endtab %}
{% endtabs %}

Examine the **while loop’s condition**.&#x20;

* Currently `num` is an odd number; therefore, `num % 2 == 0` will never be True.
* In this situation, we go into the `else` statement to execute the code block

{% tabs %}
{% tab title="Code Example" %}
```python
# Example 3: Else code block executing after the while loop condition becomes False

num = 10

while num > 0:
    print(num)
    num -= 1
else:
    print('We have reached the end.')
```
{% endtab %}

{% tab title="Output" %}
```
10
9
8
7
6
5
4
3
2
1
We have reached the en
```
{% endtab %}
{% endtabs %}

* The code above has a while loop that starts with its condition evaluating to `True`.
* This allows the while loop to execute its code block until the condition evaluates to `False`.
* Once the condition becomes `False`, we execute the `else` code block as well.
