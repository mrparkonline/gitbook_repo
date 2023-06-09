# Basic Sorting Algorithms

## Bubble Sort <a href="#bubble-sort" id="bubble-sort"></a>

A sorting algorithm that is based upon comparing pairs of values and swapping their places if necessary.

**Overall Idea:**

```
- (L→ List, i→ index, i starts at 1)    
- Look at L[i] and L[i-1] if they are not sorted, swap locations
- Repeat as you increase i and until no swap occurs
```

**Bubble Sort Demonstration:**

![Source](https://mrparkonline.github.io/figures/bubble.gif)

{% tabs %}
{% tab title="Pseudocode" %}
```
repeat until swapped is false
	swapped = false
	for i = 1 to N-1 (inclusively)
		if A[i-1] > A[i] then
			swap(A[i-1],A[i])
			swapped = true
```
{% endtab %}

{% tab title="Implementation" %}
```python
# Bubble Sort:
def bubble(array):
    swapped = True

    if not array:
        return []
    elif len(array) == 1:
        return array
    else:
        while swapped:
            swapped = False
            # Execute necessary swaps from array[1] to array[n]
            for i in range(1,len(array)):
                if array[i-1] > array[i]:
                    # swapping; set swapped to True
                    temp = array[i-1]
                    array[i-1] = array[i]
                    array[i] = temp
                    swapped = True
            # end of for
        # end of while
        return array
# end of bubble()

test = [6, 5, 3, 1, 8, 7, 3, 4]
bubble(test) # since it is a list, it will mutate it

print('Sorted:', test)
```

```
Sorted: [1, 3, 3, 4, 5, 6, 7, 8]
```
{% endtab %}
{% endtabs %}

## Insertion Sort <a href="#insertion-sort" id="insertion-sort"></a>

A sorting algorithm that iterates sorts from the bottom one element at a time.

**Overall Idea:**

* Since a singleton list is already sorted, it will grow its “sorted” list with the next value from the list
* It grabs the next value, removes it, and places in the correct location
* It does this until the list is fully sorted

**Insertion Sort Demonstration:**

![Source](https://mrparkonline.github.io/figures/insert.gif)

{% tabs %}
{% tab title="Pseudocode" %}
```
-- Let A be a List, i and j both be indexes

i = 1
while i < length(A)
	j = i
	while j > 0 and A[j-1] > A[j]
		swap A[j] and A[j-1]
		j = j - 1
	i = i + 1
```
{% endtab %}

{% tab title="Implementation" %}
```python
# Insertion Sort

def insertSort(array):
    i = 1

    if not array:
        return []
    elif len(array) == 1:
        return array
    else:
        while i < len(array):
            j = i # setting up j indexer
            while j > 0 and array[j-1] > array[j]:
                # swapping
                temp = array[j]
                array[j] = array[j-1]
                array[j-1] = temp

                # decrease j
                j -= 1
            # end of inner while
            i += 1
        # end of while
        return array
# end of insertSort()

test = [6, 5, 3, 1, 8, 7, 3, 4]
insertSort(test) # since it is a list, it will mutate it

print('Sorted:', test)
```

```
Sorted: [1, 3, 3, 4, 5, 6, 7, 8]
```
{% endtab %}
{% endtabs %}

## Selection Sort <a href="#selection-sort" id="selection-sort"></a>

A sorting algorithm that uses two lists: sorted list and unsorted list.

It brings the smallest values to the sorted list then removed the smallest value in the unsorted list .

**Overall Idea:**

* At beginning, sorted list is empty and unsorted list is full
* Choose the smaller(or largest) value from the unsorted list, and append it to the sorted list
* Repeat until unsorted list is empty

**Selection Sort Demonstration:**

![Source](https://mrparkonline.github.io/figures/select.gif)

{% tabs %}
{% tab title="Pseudocode" %}
```
-- Let A be the unsorted list, and let B be the sorted list; B starts empty

repeat until A is empty
    Target = the smallest value from A
    Append Target to B
    Remove target from A
```
{% endtab %}

{% tab title="Implementation" %}
<pre class="language-python"><code class="lang-python"><strong># Recursive Selection Sort
</strong>
def selectSort(array, result=[]):
    if not array:
        return result
    else:
        smallest = array[0]
        small_index = 0

        for i in range(1,len(array)):
            if array[i] &#x3C; smallest:
                smallest = array[i]
                small_index = i
        # end of for
        result.append(array.pop(small_index))

        return selectSort(array, result)

test = [6, 5, 3, 1, 8, 7, 3, 4]
sorted_test = selectSort(test) # the algorithm is designed to create/return a new list

print('Sorted:', sorted_test)
</code></pre>

```
Sorted: [1, 3, 3, 4, 5, 6, 7, 8]
```
{% endtab %}
{% endtabs %}

## Complexity of Bubble, Insertion, and Selection Sort. <a href="#complexity-of-bubble-insertion-and-selection-sort" id="complexity-of-bubble-insertion-and-selection-sort"></a>

The 3 sorting algorithms are learned together due to their Big-O Notation.

All 3 algorithms are classified as $$O(n^2)$$.

