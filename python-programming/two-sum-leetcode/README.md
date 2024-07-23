# Two Sum - LeetCode

## Goal

Our goal in this chapter is to analyze a competitive programming problem to breakdown the requirements for a solution.

{% hint style="info" %}
## [The Problem](https://leetcode.com/problems/two-sum/description/)

Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.
{% endhint %}

```
// Sample Runs
Example 1:

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].
Example 2:

Input: nums = [3,2,4], target = 6
Output: [1,2]
Example 3:

Input: nums = [3,3], target = 6
Output: [0,1]
```

### Problem Constraints

**Constraints (what our possible test cases will be):**

* Size constraints of the number of integers in the array -> `2 <= nums.length <= 104`
* Each individual integers will be within this range -> `-109 <= nums[i] <= 109`
* The target value will be an integer within this range -> `-109 <= target <= 109`
* **Only one valid combination of two distinct elements (item located at an index) will result to the target.**

## Problem Requirement Breakdown

* Create a [**function**](../../02-programming-in-python/defining-functions/functions.md) that can take two arguments:
  * A list of integers (we must assume that it will be unsorted)
  * An integer target value
* Traverse[^1] through the given list of integers and create a total sum based on a unique pair of integers
* Create a list with the specific indices that adds up to the given target

### Possible Solutions

1. **Generate all possible pairs of values**

* If we have all pairs of values, we can create a sum from each pair to compare it with the target.
* The indices that generated the pair that totals to the target will be our answer

2. **Subtract each value from the target, see if the difference exists in the list**

* Since a sum is a result of two operands added together, we can express it as -> `x + y = sum`
* By rearranging the equation, we can also express it as -> `y = sum - x`
* If we have the `sum` set to our given target value, and let `x` be represented by each individual values in our list, we can generate the `y` value
  * Each time we generate the `y` value, we can search the list if the `y` value exists in the list
  * If the value exists, the index of `x` and `y` will be our pair that generated our desired target value

## Connected Readings

* **Functions (**[**Link**](../../02-programming-in-python/defining-functions/functions.md)**)**
* **Loops (**[**Link**](../../02-programming-in-python/iterations/)**)**
* **List (**[**Link**](../../02-programming-in-python/tuples-and-lists/list-basics.md)**)**

[^1]: iterating over the data structure; visit individual items in a list in this scenario
