# IB Recipe Book

This page contains the IB way to code common operations found in **Paper 1 (Pre 2026)**

## Array vs Python List

#### 1. **Data Type Flexibility**

* **Array**: Typically, arrays are homogeneous, meaning all elements must be of the same data type (e.g., all integers or all floats).
* **Python List**: Lists in Python are heterogeneous, allowing you to store elements of different types (e.g., integers, strings, objects) in the same list.

#### 2. **Size and Resizing**

* **Array**: The size of an array is <mark style="color:yellow;">**fixed upon creation**</mark>. _<mark style="background-color:orange;">You cannot change its size without creating a new array</mark>_.
* **Python List**: Lists are dynamic; you can easily add or remove elements, and the list will resize automatically.

#### 3. **Memory Management**

* **Array**: Arrays are more memory-efficient for large datasets since they store elements in contiguous memory locations.
* **Python List**: Lists may use more memory due to their flexibility and the overhead of storing type information for each element.

#### 4. **Performance**

* **Array**: Generally, arrays can offer better performance for numerical computations due to their fixed size and type.
* **Python List**: While lists are versatile, they may be slower for certain operations compared to arrays, especially when dealing with large datasets.

#### 5. **Built-in Functions**

* **Array**: In languages like C, you have to implement many operations manually (like sorting or searching).
* **Python List**: Python provides a rich set of built-in methods for lists (like `.append()`, `.remove()`, and `.sort()`) that make manipulation straightforward.

### Things to avoid

1. [List Slicing](https://www.geeksforgeeks.org/python-list-slicing/)
2. Do not use any [list methods](https://www.w3schools.com/python/python\_ref\_list.asp)
3. Do not use `map(); filter(); enumerate(); max(); min(); set(); reversed()`
4. Use of set, tuple, or dictionary data types

## Creating an Array during IB Exam

```python
size = int(input()) # Set size of the array
array = [None for _ in range(0, size)]

for i in range(0, size):
    array[i] = input()
```

This code mimics the creation fixed size arrays.

### Explanation

* Variable `size` is inputted to limit the size of the array
* Variable `array` is initialized using list comprehension to create a list in python with `size` many empty spaces for future inputted value
  * Empty spaces are using the `None` keyword for empty values
* the for loop iterates `size` many times to input values at index _`i`_&#x20;
  * If inputting numeric values please type cast the `input()` function in the for loop

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

_This is where we find the index value of our max and min values_

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
# This algorithm sorts in ascending order
# let array represent an array of values
n = len(array) # Set n to length of given array
swapped = True # initialized to true to start our algorithm

while swapped == True:
    swapped = False
    for i in range(1, n):
        left = array[i-1]
        right = array[i]
        
        if left > right: # for descending order change > to <
            array[i] = left
            array[i-1] = right
            swapped = True
    # end of inner for
# end of outer while
```

## How to sort connected arrays using bubble sort

```python
# This algorithm sorts in ascending order
# let array represent an array of values
# let array2 represent another array of values

# this behaviour is common for situation where:
#     one array has names
#     the other array has values for the names
#     often called "parallel arrays"
#     they connect values from different arrays by using consistent index values

size = len(array) # Set size to length of given array
size2 = len(array2) # Set size2 to length of other array

swapped = True # initialized to true to start our algorithm

while swapped == True:
    swapped = False
    for i in range(1, n):
        left = array[i-1]
        right = array[i]
        
        if left > right: # for descending order change > to <
            array[i] = left
            array[i-1] = right
            swapped = True
            
            # Since the first array swapped values, swap the other array
            temp = array2[i]
            array2[i] = array2[i-1]
            array2[i-1] = temp
        # end of if
    # end of inner for
# end of outer while
```

## Determine the difference between one array and another

_We are trying to output a new array/collection that determines which values in one of the array does not appear in the other_

```python
# let array1 represent an array
# let array2 represent another array
# let diff represent an array that holds the non-shared values

a1_size = len(array1)
a2_size = len(array2)

for i in range(0, a1_size):
    found = False
    for j in range(0, a2_size):
        if array1[i] == array2[j]:
            found = True
            break
    # end of inner for
    
    if found == False:
        diff.append(array1[i])
# end of outer for

# We must also do this again except starting from array2
for j in range(0, a2_size):
    found = False
    for i in range(0, a1_size):
        if array1[i] == array2[j]:
            found = True
            break
    # end of inner for
    
    if found == False:
        diff.append(array2[j])
```

## Access individual digits from a number from right to left without String manipulation&#x20;

```python
# let num be an integer
# our goal is to get the individual digits
#     starting from the "ones" column
#     Example: 1234 outputs 
#       4
#       3
#       2
#       1

while num > = 0:
    current_digit = num % 10
    num = num // 10 # floor division of 10
    print(current_digit)
```
