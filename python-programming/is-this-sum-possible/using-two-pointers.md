# Using Two Pointers

```python
def twoPointers(array: list[int], target: int) -> bool:
    left = 0
    right = len(array) - 1

    while left < right:
        answer = array[left] + array[right]
        
        if answer == target:
            return True
        elif answer > target:
            right -= 1
        elif answer < target:
            left += 1

    return False  
```

Code Explanation

**Initialize Pointers:**

```python
left = 0
right = len(array) - 1
```

* `left` is initialized to the first index of the array (0).
* `right` is initialized to the last index of the array (`len(array) - 1`).

**Two-Pointer Approach:**

```python
while left < right:
    answer = array[left] + array[right]
```

* The loop continues as long as `left` is less than `right`. This condition ensures that the two pointers do not cross and that distinct elements are considered.

**Check the Sum (`answer`):**

```python
if answer == target:
    return True
```

* Calculate the sum (`answer`) of the elements at the `left` and `right` pointers.
* If `answer` equals the `target`, the function returns `True`, indicating that a pair with the desired sum has been found.

**Adjust Pointers Based on the Comparison:**

```python
elif answer > target:
    right -= 1
elif answer < target:
    left += 1
```

* If `answer` is greater than `target`, decrement the `right` pointer (`right -= 1`). This moves the `right` pointer to a smaller element, reducing the sum.
* If `answer` is less than `target`, increment the `left` pointer (`left += 1`). This moves the `left` pointer to a larger element, increasing the sum.

**How It Works:** The two-pointer method works by leveraging the sorted nature of the array. By adjusting the pointers (`left`, `right`) based on the current sum (`answer`), it efficiently narrows down the search space for finding the desired pair.&#x20;

This technique ensures that all potential pairs are considered without redundancy.

## Connected Readings

* **When to use a Two Pointer Approach by Geeksforgeeks (**[**Link**](https://www.geeksforgeeks.org/when-should-i-use-two-pointer-approach/)**)**
