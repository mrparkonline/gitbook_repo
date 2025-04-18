# Linear Search

<figure><img src="https://www.tutorialspoint.com/data_structures_algorithms/images/linear_search.gif" alt=""><figcaption><p>Animation from <a href="https://www.tutorialspoint.com/data_structures_algorithms/linear_search_algorithm.htm">TutorialsPoint</a></p></figcaption></figure>

This algorithm is used for Strings and Lists often.

* `index()` and `find()` are linear searches
* `in` and `not in` membership for **strings and lists** are linear searches

### Algorithm Classification <a href="#algorithm-classification" id="algorithm-classification"></a>

* **Big-O:** O(n) hence the name “Linear” Search … happens when the target is not found -or- target is the last value
* **Big-Omega**: O(1) very first item is the target
* **Big-Theta**: O(n/2) which simplifies to O(n) … target is found somewhere in the middle

#### Linear Search Algorithm: <a href="#linear-search-algorithm-1" id="linear-search-algorithm-1"></a>

{% tabs %}
{% tab title="Pseudocode" %}
```
    # Let L be a list of items; i be the index, and N be the number of items
    # Let T be a Target
    1 Set i to 0
    2 If L at i == Target, then return i
    3 Else increase i by 1 and repeat back to Line 2
    4 If i > N, and target has not been found, then return -1
```
{% endtab %}

{% tab title="Code" %}
```python
# Python Implementation

def linSearch(seq, target):
    ''' linSearch determines the location of the target in the sequence

    -- param
    seq : iterable/indexable data
    target : any data

    -- return
    integer
    '''

    if not seq:
        return -1
    else:
        for i in range(len(seq)):
            if seq[i] == target:
                return i
        else:
            return -1
# end of linSearch

# Example Execution
from random import seed
from random import randrange

seed(1)
#seq = [randrange(1,100) for x in range(20)]
seq = []
for x in range(20):
    seq.append(randrange(1,100))
    
print(f"Random List: \n{seq}")

print(f"--\nSearch {18} in seq: Found at {linSearch(seq, 18)}")
print(f"Search 61 in seq: Found at {linSearch(seq, 61)}")
print(f"Search 42 in seq: Found at {linSearch(seq, 42)}")
```

```
Random List:
 [18, 73, 98, 9, 33, 16, 64, 98, 58, 61, 84, 49, 27, 13, 63, 4, 50, 56, 78, 98]
--
Search 18 in seq: Found at 0
Search 61 in seq: Found at 9
Search 42 in seq: Found at -1
```
{% endtab %}
{% endtabs %}

#### Note on using a while loop <a href="#python-3-note" id="python-3-note"></a>

```python
#Method 2
def linSearch(array, target):
	ctr = 0
	while ctr < len(array):
		if array[ctr] == target:
			return ctr
		ctr += 1
	else:
		return -1
```

{% hint style="info" %}
Some of you may want to use a while loop with a counter rather than coding a for loop.

It is not recommended to do so because:

**`A while loop must check its condition on each iteration; whereas, a for loop has no looping condition to check at every iteration.`**
{% endhint %}
