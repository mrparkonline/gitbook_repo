# Is the dataset sorted?

_This is not required for the given problem, but a very simple algorithm to implement_.

```python
# A function to determine if an array of integer is sorted

def isSorted(array : list[int]) -> bool:
    if len(array) <= 1:
        return True
    else:
        for i in range(1, len(array)):
            if array[i-1] > array[i]:
                return False
        # end of for
        return True
# end of isSorted()

list1 = [1,2,3]
list2 = [3,1,4,1,5,9]
print(f"Is {list1} sorted? {isSorted(list1)}")
print(f"Is {list2} sorted? {isSorted(list2)}")
```

#### Function Definition: `isSorted`

The function `isSorted` takes a list of integers as an input and returns a boolean indicating whether the list is sorted in non-decreasing order.

```python
def isSorted(array: list[int]) -> bool:
```

* **`array: list[int]`:** This is a type annotation indicating that the parameter `array` is expected to be a list of integers.
* **`-> bool`:** This indicates that the function will return a boolean value (`True` or `False`).

1. **Base Case:**

```python
if len(array) <= 1:
    return True
```

* If the length of the array is 0 or 1, the function returns `True`.&#x20;
* A list with 0 or 1 element is trivially sorted because there are no pairs of elements to compare.

2. **Loop Through the Array:**

```python
for i in range(1, len(array)):
    if array[i - 1] > array[i]:
        return False
```

* The function iterates through the array starting from the second element (`i = 1`) to the last element (`i = len(array) - 1`).
* **Comparison:**
  * For each index `i`, it compares the element at `array[i-1]` with the element at `array[i]`.
  * If `array[i-1]` is greater than `array[i]`, the function returns `False` immediately, indicating that the list is not sorted in non-decreasing order.

3. **End of the For Loop:**

```python
return True
```

* If the loop completes without finding any elements that are out of order, the function returns `True`, indicating that the list is sorted.
