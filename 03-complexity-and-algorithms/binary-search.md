# Binary Search

{% embed url="https://www.youtube.com/watch?v=KXJSjte_OAI" %}

<figure><img src="https://www.mathwarehouse.com/programming/images/binary-vs-linear-search/binary-and-linear-search-animations.gif" alt=""><figcaption><p><a href="https://mathwarehouse.com/programming/gifs/binary-vs-linear-search.php">Image Source</a></p></figcaption></figure>

A searching algorithm that is designed to search from a sorted list.

**Idea:**

* Compare the target with the middle most value
* If not found, eliminate the half where the target cannot exist

**Cons/Caveat:**

* The database must be comparable and sortable

### Algorithm Demonstration <a href="#algorithm-demonstration" id="algorithm-demonstration"></a>

* First is a binary search and showing how it’d work
* Second is a sequential search which is the same as a linear search

### Complexity of Binary Search <a href="#complexity-of-binary-search" id="complexity-of-binary-search"></a>

Big O Notation: $$O(logn)$$

We are splitting the dataset continuously into halves until we hit our target or not find our target.

### Algorithm <a href="#algorithm" id="algorithm"></a>

{% tabs %}
{% tab title="Pseudocode" %}
```
Let A be a sorted array; N be length of A; T be searching target

    1. Set Left=0 and Right=N-1
    2. while Left <= Right:
    3. Set Middle to the floor of (Left + Right)/2
    4. If A[Middle] < T, set Left = middle+1 and go to step 2
    5. If A[Middle] > T, set Right = middle-1 and go to step 2
    6. If A[Middle] == T, return Middle as search is done
```
{% endtab %}

{% tab title="Non-recursive Solution" %}
```python
# Non Recursive Binary Search

def binSearch(array, target):
    left = 0
    right = len(array)-1

    while left <= right:
        middle = (left+right) // 2

        if array[middle] == target:
            return middle
        else:
            if array[middle] < target:
                left = middle + 1
            else:
                right = middle - 1
    else:
        return -1
# end of binSearch

test_set = [1, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59]

print('Search for 37:', binSearch(test_set, 37))
print('Search for 21:', binSearch(test_set, 21))
```

```
Output:
Search for 37: 11
Search for 21: -1
```
{% endtab %}

{% tab title="Recursive Solution" %}
```python
# Tail Recursive Binary Search

def r_binSearch(array, target, track=0):
    left = 0
    right = len(array)-1

    if not array:
        return track
    elif len(array) == 1 and array[0] != target:
        return -1
    else:
        middle = (left + right) // 2

        if array[middle] == target:
            return track+middle
        elif array[middle] < target:
            return r_binSearch(array[middle+1:], target, track + middle + 1)
        else:
            return r_binSearch(array[:middle], target, track)

# end of r_binSearch

test_set = [1, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59]

print('Search for 37:', r_binSearch(test_set, 37))
print('Search for 21:', r_binSearch(test_set, 21))
```

```
Output:
Search for 37: 11
Search for 21: -1
```
{% endtab %}
{% endtabs %}
