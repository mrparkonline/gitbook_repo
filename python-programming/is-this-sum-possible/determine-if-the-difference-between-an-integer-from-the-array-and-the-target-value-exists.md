# Determine if the difference between an integer from the array and the target value exists

## Linear Search Solution

```python
def possibleSum1(array: list[int], target: int) -> bool:
    # Linear Search Method
    for i in range(len(array)):
        current = array[i]
        diff = target - current
        
        # search diff from i+1 onwards
        for j in range(i+1, len(array)):
            if array[j] == diff:
                return True
    return False
```

**Outer Loop:**

```python
for i in range(len(array)):
    current = array[i]
    diff = target - current
```

* The outer loop iterates over each element in `array` with the index `i`.
* `current = array[i]`: Assigns the value at the current index `i` to the variable `current`.
* `diff = target - current`: Calculates the difference `diff` between the target and the current element. This difference is the value we need to find in the rest of the array to sum with `current` to reach the `target`.

**Inner Loop:**

```python
for j in range(i+1, len(array)):
    if array[j] == diff:
        return True
```

* The inner loop starts from the index `i + 1` and iterates to the end of the array. This ensures that we are not using the same element twice and that we find distinct pairs.
* **Comparison:**
  * For each `j`, it checks if `array[j]` equals `diff`.
  * If `array[j] == diff`, it means the current element `array[i]` and `array[j]` together sum up to the `target`. The function immediately returns `True`.

**Return `False`:**

```python
return False
```

* If the function completes the outer loop without finding any pair of elements that sum up to the `target`, it returns `False`. This indicates that no such pair exists in the array.

## Binary Search Solution

```python
def binarySearch(array: list[int], target: int, start:int = 0) -> int:
    left = start
    right = len(array)-1

    while left <= right:
        middle = (left + right) // 2
        if array[middle] == target:
            return middle
        elif array[middle] > target:
            right = middle - 1
        else:
            left = middle + 1
    # end of while
    
    return -1 #  If the target is not found in the array, return -1 as an error code.
# end of binSearch()

def possibleSum2(array: list[int], target: int) -> bool:
    # Binary Search Method
    for i in range(len(array)):
        current = array[i]
        diff = target - current
    
        if binarySearch(array, diff, i+1) != -1:
            return True
    # end of for
    return False # If the loop completes without finding any such pair, return False
# end of possibleSum2
```

### Code Explanation

```python
def binarySearch(array: list[int], target: int, start: int = 0) -> int:
```

* **`array: list[int]`:** A sorted list of integers.
* **`target: int`:** The integer value to search for in the list.
* **`start: int = 0`:** The starting index for the search. Defaults to 0.
* **`-> int`:** The function returns the index of the target if found; otherwise, it returns -1.

**Function Logic**

**Initialize `left` and `right` Pointers:**

```python
left = start
right = len(array) - 1
```

* `left` starts at the `start` index (default is 0).
* `right` starts at the last index of the array (`len(array) - 1`).

**Binary Search Loop:**

```python
while left <= right:
    middle = (left + right) // 2
```

* The loop continues as long as `left` is less than or equal to `right`.
* `middle` is the index of the middle element in the current search range.

**Check Middle Element:**

```python
if array[middle] == target:
    return middle
```

* If the middle element equals the `target`, the function returns the `middle` index.

**Adjust Search Range:**

```python
if array[middle] > target:
    right = middle - 1
else:
    left = middle + 1
```

* If the middle element is greater than the `target`, search in the left half by updating `right` to `middle - 1`.
* If the middle element is less than the `target`, search in the right half by updating `left` to `middle + 1`.

### Function: `possibleSum2`

```python
def possibleSum2(array: list[int], target: int) -> bool:
```

* **`array: list[int]`:** A sorted list of integers.
* **`target: int`:** The target sum to find.
* **`-> bool`:** The function returns `True` if there are two distinct numbers in the array that sum to `target`; otherwise, `False`.

**Function Logic**

**Iterate Over the Array:**

```python
for i in range(len(array)):
    current = array[i]
    diff = target - current
```

* Loop over each element in the array with index `i`.
* `current` is the current element.
* `diff` is the difference between the `target` and the `current` element, representing the value needed to reach the `target`.

**Use `binarySearch` to Find `diff`:**

```python
if binarySearch(array, diff, i + 1) != -1:
    return True
```

* Call `binarySearch` to search for `diff` in the subarray starting from index `i + 1` to the end of the array.
* If `binarySearch` returns a valid index (not -1), it means there exists an element `diff` in the array such that `current + diff = target`. The function returns `True`.
