# Longest Common Prefix - LeetCode

## Goal

Our goal in this chapter is to analyze a string related competitive programming problem to breakdown the requirements for a solution.

{% hint style="info" %}
## [The Problem](https://leetcode.com/problems/longest-common-prefix/description/)

Write a function to find the longest common prefix string amongst an array of strings.

If there is no common prefix, return an empty string `""`.
{% endhint %}

```
// Example 1:

Input: strs = ["flower","flow","flight"]
Output: "fl"

// Example 2:

Input: strs = ["dog","racecar","car"]
Output: ""
Explanation: There is no common prefix among the input strings.
```

### Problem Constraints

**Constraints (what our possible test cases will be):**

* Number of different words -> `1 <= words.length <= 200`
* The word length of each words -> `0 <= words[i].length <= 200`
* Each word in our dataset will consists of only lowercase English letters or an empty string.

## Problem Requirement Breakdown

* Create a [**function**](../../02-programming-in-python/defining-functions/functions.md) that takes a single argument:
  * A list of strings
* Compare different prefixes to find matching patterns
* Return a common prefix if found, otherwise return an empty string

### Possible Solutions

1. **Compare all possible prefixes**

* Grab the first word of the dataset
  * We will be creating all possible for prefixes from this word
* Compare the rest of the dataset and see if the first word's prefixes can be a prefix from each word in the dataset
  * If so, return the longest prefix

2. **Create the longest common prefix with the direct neighbour**

* Assume that the longest prefix is the first word of the dataset
* Compare that second word in the list with the current long prefix and create a new longest prefix possible
* Do this with each subsequent neighbours
* At any point the longest prefix is empty, return empty string
* If there are no more neighbours, return the prefix

3. **Look at each strings vertically to see if they match**

```
0 1 2 3 4 5 6
f l o w
f l o w e r
f l o w e r s
```

## Connected Readings

* **Functions (**[**Link**](../../02-programming-in-python/defining-functions/functions.md)**)**
* **Loops (**[**Link**](../../02-programming-in-python/iterations/)**)**
* **List (**[**Link**](../../02-programming-in-python/tuples-and-lists/list-basics.md)**)**
* **Strings (**[**Link**](../../02-programming-in-python/strings/)**)**
