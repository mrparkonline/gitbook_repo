# Merge Sort

A comparison-based algorithm that sorts a given dataset.

It is classified as a **“divide and conquer”** algorithm.

1. **Divide**: The algorithm begins by dividing the input array into two roughly equal-sized subarrays. This process continues recursively until the subarrays become small enough to be considered sorted individually (usually when they contain only one element).
2. **Conquer**: Once the subarrays are small enough, they are considered sorted by definition. If the subarray has more than one element, the algorithm recursively applies the merge sort algorithm to further divide it. This step ensures that every element in the array is individually sorted.
3. **Merge**: After all the recursive divisions and sorting are complete, the algorithm starts merging the sorted subarrays back together to produce a single sorted array. It compares the elements from each subarray and selects the smallest (or largest, depending on the sorting order) element to place in the final sorted array. The process continues until all the elements from the subarrays are merged.
4. **Finalize**: Once the merging process is complete, the array is fully sorted. The sorted array is the output of the merge sort algorithm.

### Merge Sort Demonstration

<figure><img src="https://upload.wikimedia.org/wikipedia/commons/c/cc/Merge-sort-example-300px.gif" alt=""><figcaption><p><a href="https://upload.wikimedia.org/wikipedia/commons/c/cc/Merge-sort-example-300px.gif">Source</a></p></figcaption></figure>

**Complexity of Merge Sort:**

$$O(nlogn)$$ for all best, average and worst case scenarios.

{% tabs %}
{% tab title="Pseudocode" %}
```
-- Let A be an unsorted list, n represent size of A

function: divider(A)
    Create two empty lists called Left and Right

    Get Midpoint at n/2 - 1,
        - all values before and include the midpoint is Left list
        - all values after midpoint is Right list

    Update Left to divider(Left) ... recursive call
    Update Right to divider(Right) ... recursive call

    return merge(Left, Right)

-- Let X and Y be sorted List called from divider()

function: merge(X, Y)
    Create empty list called Sorted

    While both x and y are not empty
        if X and Y are both non empty
            compare X[0] and Y[0]
                add the smaller value to Sorted
                removed the respective
    if X is empty and Y is not empty
        add all Y values to Sorted

    if Y is empty and X is not empty
        add all X values to Sorted

    return Sorted
```
{% endtab %}

{% tab title="Python Implementation" %}
```python
# Recursive Merge Sort Python Implementation
# Top Down Approach


def mergeSort(array):
    if len(array) <= 1:
        return array
    # end of base case

    left = [] # Division of array : left half
    right = [] # Divsion of array : right half

    for i in range(len(array)):
        if i < (len(array) // 2):
            left.append(array[i])
        else:
            right.append(array[i])
    # end of division

    # recursive mergeSort of left and right
    left = mergeSort(left)
    right = mergeSort(right)

    return merge(left, right)
# end of mergeSort()

def merge(left, right):
    result = []
    i = 0 # index for left
    j = 0 # index for right

    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1
    # end of handling left and right

    while i < len(left):
        result.append(left[i])
        i += 1

    while j < len(right):
        result.append(right[j])
        j += 1

    return result
# end of merge()

test = [6, 5, 3, 1, 8, 7, 3, 4]

sorted_test = mergeSort(test) # creates a new sorted list
print('Sorted:', sorted_test)
```

```
Sorted: [1, 3, 3, 4, 5, 6, 7, 8]
```
{% endtab %}
{% endtabs %}
