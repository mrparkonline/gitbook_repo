# For Loops w/ Numeric Sequences

With studying Computer Science, we can use a lot of integers. By using `range()` function along with a `for loop`, we can start to analyze integer based sequences.

## `range()` function <a href="#range-function" id="range-function"></a>

* The `range()` function can take 3 different arguments and it must have atleast **1 argument**.
* The `range()` function is a function that generates an _iterable_ sequence of integers in an arithmetic progression.

{% hint style="info" %}
**IMPORTANT NOTE:** the result of a `range()` function is not printable by itself.&#x20;

It must be converted to string or a list if you want to see the **entire sequence**.
{% endhint %}

**Different Behaviours of:** `range()`

{% hint style="info" %}
_NOTE: `[` means inclusive, `(` means exclusive_ mathematically.&#x20;

Read more at this [link](http://zonalandeducation.com/mmts/miscellaneousMath/intervalNotation/intervalNotation.html).
{% endhint %}

1. `range(n)` returns a sequence of `[0,n)`
2. `range(a,b)` returns a sequence of `[a,b)`; if a == b, it is an empty sequence
3. `range(start, end, interval_value)` returns a sequence of `[start,end)`, but the sequence will approach the end value by adding each step with the interval value. if the `interval_value` is not specified, it is assumed to be 1.

_NOTE: `range()` never includes the last/ending value._

### **Examples of range()**

```python
range(10) :: contains 0, 1, 2, 3, 4, 5, 6, 7, 8, 9

range(10,21) :: contains 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20

range(2, 20, 4) :: contains 2, 6, 10, 14, 18

range(100, 0, -10) :: contains 100, 90, 80, 70, 60, 50, 40, 30, 20, 10

range(-10, -15, -1) :: contains -10, -11, -12, -13, -14

range(-5, 6) :: contains -5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5
```

## For Loops with `range()` <a href="#for-loops-with-range" id="for-loops-with-range"></a>

Since `range()` returns an iterable sequence, we can look through each individual values in it with a `for loop`.

{% tabs %}
{% tab title="Code" %}
```python
# Example 1
# For Loops with range()

for num in range(10):
    print('Current Number:', num)

# Examine that the iterating variable: num is going to represent each number
# in the sequence in order for each iteration of the for loop
```
{% endtab %}

{% tab title="Example" %}
```
Current Number: 0
Current Number: 1
Current Number: 2
Current Number: 3
Current Number: 4
Current Number: 5
Current Number: 6
Current Number: 7
Current Number: 8
Current Number: 9
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Code" %}
```python
# Example 2
# For Loops with range()

for negatives in range(-5,0):
    print('Negative values:', negatives)
```
{% endtab %}

{% tab title="Output" %}
```
Negative values: -5
Negative values: -4
Negative values: -3
Negative values: -2
Negative values: -1
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Code" %}
```python
# Example 3
# Finding the factors a number

target_value = 12

# Notice that we increase our end value of our range to include our target_value
for divider in range(1, target_value+1):
    if target_value % divider == 0:
        # found a factor
        print(divider, 'is a factor of', target_value)
```
{% endtab %}

{% tab title="Example" %}
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
