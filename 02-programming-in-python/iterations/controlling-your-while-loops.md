# Controlling Your While Loops

## Flag Based While Loop <a href="#flag-based-while-loop" id="flag-based-while-loop"></a>

To control when to exit a while loop, we can also a flag like variable to make the condition become False based on user input.

```python
    flag = True

    while flag:

        Your Code Here

        user_input = input('Do you want an exit? (y/n): ')
        if user_input in 'yY':
            flag = False
   # end of while
```

This type of formatting a while loop help us to potentially loop forever, but at the end of the code block we get to choose if we want to iterate again.

* At the bottom of the while loop, we have an input that asks the user if they want to exit
* If they do want to exit, our looping condition would turn to `false` and end the loop
* Otherwise; the loop continues to execute its code block

## While Loop and Numbers <a href="#while-loop-and-numbers" id="while-loop-and-numbers"></a>

We can manipulate variables to represent a range of numbers by repetitively applying arithmetic operators.

#### Assignment Operators <a href="#recall-assignment-operators" id="recall-assignment-operators"></a>

```python
    a = b   # (Assignment)
    a += b  # (Add & Assign)
    a -= b  # (Subtract & Assign)
    a *= b  # (Multiply & Assign)
    a /= b  # (Divide & Assign)
    a //= b # (Floor Divide & Assign)
    a **= b # (Exponentiate & Assign)
    a %= b  # (Modulo & Assign)
```

These operators will manipulate/update the left variable with the result of the arithmetic operation with the right operand.

If we can use these inside a while loop code block, we can repetitively change the variable to make a condition become False to end the while loop.

### Code Examples:

{% tabs %}
{% tab title="Code" %}
```python
# Counting from 1 to 10

num = 1
while num <= 10:
    print(num)
    num += 1
# end of while
```
{% endtab %}

{% tab title="Output" %}
```
1
2
3
4
5
6
7
8
9
10
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Code" %}
```python
# Collatz Sequence
# The conjecture of the collatz sequence is that any number following the set of rules will always end up at 1

# Rule:
# If N is even, divide it by 2
# If N is odd, multiply by 3 then add 1

num = 13 # a random starting value

while num != 1:
    print(num)

    if num % 2 == 0:
        num //= 2
    else:
        num *= 3
        num += 1
# end of while
print(num)
```
{% endtab %}

{% tab title="Output" %}
```
13
40
20
10
5
16
8
4
2
1
```
{% endtab %}
{% endtabs %}
