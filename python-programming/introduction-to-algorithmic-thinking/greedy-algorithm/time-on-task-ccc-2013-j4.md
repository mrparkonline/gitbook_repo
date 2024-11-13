# Time on Task (CCC 2013 J4)

{% embed url="https://www.youtube.com/watch?v=nFB_z5VMJ4w" %}

## Problem

You have been asked by a parental unit to do your chores.

Each chore takes a certain amount of time, but you may not have enough time to do all of your chores, since you can only complete one chore at a time. You can do the chores in any order that you wish.

What is the largest amount of chores you can complete in the given amount of time?

### Input Specifications

The first line of input consists of an `integer T (0 <= T <= 100000)`, which is the total number of minutes you have available to complete your chores.

The second line of input consists of an `integer C (0 <= C <= 100)`, which is the total number of chores that you may choose from.&#x20;

The next **`C`** lines contain the (positive integer) number of minutes required to do each of these chores. You can assume that each chore will take at most 100,000 minutes.

### **Output Specification**

The output will be the maximum number of chores that can be completed in time T.

{% tabs %}
{% tab title="Sample Input" %}
```
6
3
3
6
3
```
{% endtab %}

{% tab title="Output and Explanation" %}
```
2
```

Chores must be completed in at most 6 minutes.&#x20;

* There are 3 chores available.&#x20;
  * The first chore takes 3 minutes.&#x20;
  * The second chore takes 6 minutes.&#x20;
  * The third chore takes 3 minutes.&#x20;
* The answer is 2 since only 2 of these chores can be completed in 6 minutes.&#x20;

Specifically, the first and last chore can be completed in the allowable time. It is not possible to complete all 3 chores in 6 minutes.
{% endtab %}
{% endtabs %}

## Solution

