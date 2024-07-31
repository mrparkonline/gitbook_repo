# Searching for a value

## Linear/Sequential Search

```
PSEUDOCODE

Let L represent an array of values
    Let n represent the size of the array
Let T represnet target value T, 
Let i represent index of L

1. Set i to 0.
2. If L[i] = T, the search terminates successfully; return i.
3. If i < n, Increase i by 1 and go to step 2. 
4. If i == n, the search terminates unsuccessfully.
```

[**Linear Search**](https://en.wikipedia.org/wiki/Linear\_search) is the act of looking through a collection from the start and determining the index of the value you are searching for.

* Best Case Scenario: The first item is the target value
* Average Case: The target is somewhere near the middle of the dataset
* Worst Case: The target is not found, and you have analyzed every single value

_By encountering the worst case scenario, we can potentially have a slow algorithm._

{% hint style="info" %}
If the array had a million data points, and our target value is not one of the given value, the algorithm would be required to make a million comparisons to determine it is not in the array.

The study of efficiency of algorithm is called [**Complexity Analysis**](https://en.wikipedia.org/wiki/Computational\_complexity)**.**
{% endhint %}

The search algorithm is called "linear" because it individually searches for the target from start to end.&#x20;

## Binary Search

```
PSEUDOCODE

Let A represent a sorted array of values
    Let n represent the size of A
Let L represent left index point
Let R represent right index point
Let m represent middle index point
Let T represent the target value of interest

1.  L = 0
2.  R = n − 1
3.  while L <= R do:
4.      m := floor((L + R) / 2)
5.      if A[m] < T then
6.          L := m + 1
7.      else if A[m] > T then
8.          R := m − 1
9.      else:
10.         return m
11. return unsuccessful
```

[**Binary Search**](https://en.wikipedia.org/wiki/Binary\_search) is a searching algorithm that works only on sorted and comparable dataset. It is considered to be significantly faster than linear search because it ignores where the target value cannot exist in the dataset by comparing the target with its generated midpoint.

The midpoint changes every iteration to shrink the search range within the dataset until the target is found or not found.

### Linear vs Binary Search

```
Let A be a list of integers from 1 to 100 inclusively.
Let T be a value of 77

LinearSearch(A, T) would do 77 comparisons to determine that 77 exists at index 76

BinarySearch(A, T) would do the following comparisons:
Comparison 1 -> Is T a value of 50? (No) ... 50 = (1 + 100) / 2 rounded down
Comparison 2 -> Is T > 50? (Yes)
    - At this point our search range was updated to 51 to 100 rather than 1 to 100

Comparison 3 -> Is T a value of 75? (No)
Comparison 4 -> Is T > 75? (Yes)
    - At this point our search range is 76 to 100
    
Comparison 5 -> Is T a value of 88 (No)
Comparison 6 -> Is T > 88 (No)
    - At this point our search range is 76 to 88

Comparison 7 -> Is T a value of 81 (No)
Comparison 8 -> Is T > 81 (No)
    - At this point our search range is 76 to 81

Comparison 9 -> Is T a value of 78 (No)
Comparison 10 -> Is T > 78 (No)
    - At this point our search range is 76 to 78

Comparison 10 -> Is T a value of 77 (Yes)
    - The search is now completed
```

As the dataset gets bigger, the linear search will do more comparisons compared to binary search. This classifies that binary search is a faster algorithm than linear search.

The weakness of binary search are the following:

* The dataset must be sorted (which increases complexity if the dataset is not sorted)
* The dataset must be comparable
* The algorithm cannot be used to find multiple instances or duplicates; it can only generate a single answer

## Connected Reading

* **Linear Search (**[**Link**](../../03-complexity-and-algorithms/linear-search.md)**)**
* **Binary Search (**[**Link**](../../03-complexity-and-algorithms/binary-search.md)**)**
* **Big-O Notation (**[**Link**](../../03-complexity-and-algorithms/big-o-notation.md)**)**
