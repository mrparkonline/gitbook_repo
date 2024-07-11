# Exercise Set 1

## Comprehension Questions



## Programming Questions

{% embed url="https://www.youtube.com/watch?v=f0b0OsKkwmU" %}

### 1. Introductory Python Program

You are to create a python program that reads three user inputted data:

1. **User's first name** (Example: "Marshall")
2. **User's last name** (Example: "Park")
3. **User's birth year** (Example: 2020)

With the given data, the program will greet the user, state their age, and determine if the user is old enough to drink in [Ontario, Canada](https://www.agco.ca/en/alcohol/legal-drinking-age-and-photo-id).

**Sample execution of the program:**

```
# Inputs:
Marshall
Park
2020
# Outputs:
Hello Marshall Park.
You are 4 years old.
You are not old enough to drink.
```

**Solution Code (**[**Link**](https://github.com/mrparkonline/ics4u\_2023F/raw/main/video\_solution/intro.py)**)**

### 2. Squares ([CCC 2004 - J1](https://dmoj.ca/problem/ccc04j1/pdf))

{% embed url="https://www.youtube.com/watch?v=I3XNC6ilBtM" %}

Write a program that inputs the number of tiles and then prints out the maximum side length. You may assume that the number of tiles is less than ten thousand.&#x20;

([Please click on the given link for an in-depth question explanation](https://dmoj.ca/problem/ccc04j1/pdf))

_CCC is a_ [_Canadian Computing Competition_](https://cemc.uwaterloo.ca/contests/ccc-cco.html) _held by University of Waterloo._

**Solution Code (**[**Link**](https://raw.githubusercontent.com/mrparkonline/ics4u\_2023F/main/video\_solution/vid03.py)**)**

### 3. Painting Fences

{% embed url="https://www.youtube.com/watch?v=n679zhVXJwY" %}

You are to create a program that determines how many paint cans we’d need.

* Each plank of the fence requires one paint can.
* Your supplier only sells paint cans by the dozen (12) for $14.95.
* There are 3 fenced sections, and their length will be denoted by a series of ‘F’ for each fence plank.

Output how many cans you’d need, how many paint cans you have leftover, and how much it would cost.

{% tabs %}
{% tab title="Sample Run 1" %}
```
Sample Input:
FF
FFFF
FFFFFF

Sample Output:
12
0
14.95
```
{% endtab %}

{% tab title="undefined" %}
```
Sample Input:
FFFFFFFFFFFF
FFFFFFFF
FFFFFFFFFFFFFFFFFFFFF

Sample Output:
41
7
59.8
```
{% endtab %}
{% endtabs %}

**Solution Code (**[**Link**](https://raw.githubusercontent.com/mrparkonline/ics4u\_2023F/main/video\_solution/vid04.py)**)**

### 4. Selling Cookies

{% embed url="https://www.youtube.com/watch?v=Mnb8MY5_pBc" %}

**The program takes 2 user inputs:**

* `start` → the amount of money we had before selling cookies
* String of `b` or `c`
  * `num_cookies` → a string of character ‘c’s to denote the number of cookies sold
    * Example: `cccccc` → 6 cookies!
  * `num_big` → a string of character ‘b’s to denote the number of big cookies sold
    * Example: `bbb` → 3 big cookies!

**The program should output:**

1. Number of total cookies sold
2. Profit (which is calculated as profit = sales - cost of cookie)
   1. Cost of Normal Cookie per cookie → $1.25
   2. Cost of Big cookie per cookie → $2.00
   3. To make a normal cookie → $0.50
   4. To make a big cookie → $0.75
3. Total amount of money after selling cookies

**Solution Code (**[**Link**](https://raw.githubusercontent.com/mrparkonline/ics4u\_2023F/main/video\_solution/vid05.py)**)**
