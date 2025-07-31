# Sorting Algorithms

A sorting algorithm is a method or process used to arrange elements in a particular order, typically in numerical or lexicographical order. Sorting is a fundamental operation in computer science and is used to organize data for more efficient searching, retrieval, and manipulation.

## Example: Selection Sort

**How it works:**

1. Find the smallest card. Swap it with the first item.
2. Find the second-smallest card. Swap it with the second item.
3. Find the third-smallest card. Swap it with the third item.
4. Repeat finding the next-smallest card, and swapping it into the correct position until the array is sorted.

**Python Code for Selection Sort:**

```python
def selectionSort(array):
    for i in range(len(array)):

        smallest = None
        location = 0
        
        for j in range(i+1, len(array)):
            if smallest is None:
                smallest = array[j]
                location = j
            elif array[j] < smallest:
                smallest = array[j]
                location = j
        # end of inner for
        
        if smallest < array[i]:
            # Python Swap
            array[i], array[location] = array[location], array[i]
    # end of outer loop
    return array
# end of selectionSort()

def selectionSort2(array):
    # A two list approach
    sorted_list = []
    
    while array:
        smallest = min(array)
        array.remove(smallest)
        sorted_list.append(smallest)
    
    return sorted_list
# end of selectionSort2()
```

### What sorting algorithm does the Python use?

There is a built-in sorting function called `sorted()` and lists have a method called `.sort()`

> Timsort is a [hybrid](https://en.wikipedia.org/wiki/Hybrid\_algorithm), [stable](https://en.wikipedia.org/wiki/Category:Stable\_sorts) [sorting algorithm](https://en.wikipedia.org/wiki/Sorting\_algorithm), derived from [merge sort](https://en.wikipedia.org/wiki/Merge\_sort) and [insertion sort](https://en.wikipedia.org/wiki/Insertion\_sort), designed to perform well on many kinds of real-world data. It was implemented by [Tim Peters](https://en.wikipedia.org/wiki/Tim\_Peters\_\(software\_engineer\)) in 2002 for use in the [Python programming language](https://en.wikipedia.org/wiki/Python\_\(programming\_language\)).
>
> [Wikipedia](https://en.wikipedia.org/wiki/Timsort)

Timsort is classified to be faster than our example of a selection sort.

#### Using `sorted()`

```python
numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5]
sorted_numbers = sorted(numbers)
print(sorted_numbers)
# Output: [1, 1, 2, 3, 3, 4, 5, 5, 5, 6, 9]
```

#### Using `.sort()`

```python
numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5]
numbers.sort()
print(numbers)
# Output: [1, 1, 2, 3, 3, 4, 5, 5, 5, 6, 9]
```

## Connected Readings

* **Basic Sorting Algorithms (**[**Link**](../../introduction-to-algorithmic-thinking/basic-algorithms/basic-sorting-algorithms.md)**)**
* **Merge Sort (**[**Link**](../../introduction-to-algorithmic-thinking/divide-and-conquer/merge-sort.md)**)**
* **"How does timsort work? - Baeldung" (**[**Link**](https://www.baeldung.com/cs/timsort)**)**
