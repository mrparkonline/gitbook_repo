# IB Recipe Book

This page contains the IB way to code common operations found in **Paper 1 (Pre 2026)**

## Find the maximum/minimum value in an array

_This is assuming we can't use max() nor min()_

```python
# let array represent an array of values
n = len(array) # Set n to length of given array

# Initialize variables to hold the first value
smallest = array[0]
largest = array[0]

# Logic: compare against the variable above, and update if necessary
for i in range(1, n):
    if array[i] < smallest:
        smallest = array[i]
    
    if array[i] > largest:
        largest = array[i]

# If you only need either max or min, you can remove the unneeded if statement
# This can also be put into a function/sub-program if needed
```

## Find the maximum/minimum value's index in an array

This is where we find the index value of our max and min values

```python
# let array represent an array of values
n = len(array) # Set n to length of given array

# Initialize variables to hold the first value
smallest = array[0]
largest = array[0]

smallest_location = 0 # smallest index holder
largest_location = 0 # largest index holder

# Logic: compare against the variable above, and update if necessary
for i in range(1, n):
    if array[i] < smallest:
        smallest = array[i]
        smallest_location = i
    
    if array[i] > largest:
        largest = array[i]
        largeest_location = i
```

## Calculate the average from an array of values

```python
# let array represent an array of values
n = len(array) # Set n to length of given array

total_sum = 0 # initialize total_sum variable

for i in range(0, n):
    total_sum = total_sum + array[i]

average = total_sum / n
```

## Linear search an array to find a target value

```python
def linear_search(array, target):
    # let array represent an array of values
    # let target the value we search for
    n = len(array) # Set n to length of given array
    
    for i in range(0, n):
        if array[i] == target:
            return i
    # end of for
    return -1 # let -1 be an error code for not found
# end of linear search
```

## Binary search an array to find a target value

```python
def binary_search(array, target):
    # let array represent an array of values that are sorted
    # let target the value we search for
    n = len(array) # Set n to length of given array
    left = 0
    right = n - 1
    
    while left <= right:
        mid = (left + right) // 2 # specify that // means a floor division
        if array[mid] < target:
            left = mid + 1
        elif array[mid] > target:
            right = mid - 1
        else:
            return mid
    # end of while
    return -1 # let -1 be an error code for not found
# end of linear search
```

## How to sort an array of data using Bubble Sort

```python
# let array represent an array of values
n = len(array) # Set n to length of given array
swapped = True # initialized to true to start our algorithm

while swapped == True:
    swapped = False
    for i in range(1, n):
        left = array[i-1]
        right = array[i]
        
        if left > right:
            array[i] = left
            array[i-1] right
            swapped = True
    # end of inner for
# end of outer while
```





