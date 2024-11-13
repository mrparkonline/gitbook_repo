# Is This Sum Possible?

## Goal

Our goal in this chapter is to introduce basic algorithms related to sorting and searching through a given problem and example of solution pathways.

{% hint style="info" %}
## The Problem

Given an array of integers that are sorted in increasing order, determine if it is possible to have a unique-indexed pair of numbers that adds up to a given target value.
{% endhint %}

```
// Sample Runs
Input: numbers = [2,7,11,15], target = 9
Output: True
Explanation: The sum of 2 and 7 is 9. 

Input: numbers = [2,3,4], target = 6
Output: True
Explanation: The sum of 2 and 4 is 6. 

Input: numbers = [-1,0], target = -1
Output: True
Explanation: The sum of -1 and 0 is -1.

Input: numbers = [1, 2, 3, 9], target = 8
Output: False
Explanation: No two combination of values add up to 8.

Input: numbers = [1, 2, 4, 4], target = 8
Output: True
Explanation: 4 + 4 is 8; moreover, 
    index 2 and index 3 contain duplicates of 4 which allows a sum of 8
```

### Problem Constraints

* The array can contain positive and negative integers
* The array can contain duplicate values
* The index of the two operands cannot be equal

## Solution Ideas

1. Determine if the difference between an integer from the array and the target value exists

```
Example:

numbers = [2,7,11,15], target = 9

Target - numbers[i] = Difference -> 9 - 2 = 7
7 does exist in numbers and it is not the same index of the current index.

The target sum is possible!
```

**Programming Concepts ->** `Searching for a value`

2. **Two Pointer Solution**

_This solution optimizes the previous solution by taking advantage of the dataset being sorted._

**Programming Concepts**

* Basic Sorting Algorithm
* Using Two Pointers

## Connected Readings

* **Functions (**[**Link**](../../../02-programming-in-python/defining-functions/functions.md)**)**
* **Loops (**[**Link**](../../../02-programming-in-python/iterations/)**)**
* **List (**[**Link**](../../../02-programming-in-python/tuples-and-lists/list-basics.md)**)**
