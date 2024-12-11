# Create the longest common prefix with the direct neighbour

## Solution Breakdown

* Assume that the longest prefix is the first word of the dataset
* Compare that second word in the list with the current long prefix and create a new longest prefix possible
* Do this with each subsequent neighbours
* At any point the longest prefix is empty, return empty string
* If there are no more neighbours, return the prefix

### Example of looking at differences

```
sample
```

explanation

### Pseudocode

```
# INSERT PSEUDOCODE HERE
```

## Python Solution

```python
def longestCommonPrefix(words: list[str]) -> str:
    # Base Case: list of words only has 1 value
    if len(words) == 1:
        return words[0]
    
    prefix = words[0]
    
    for i in range(1, len(words)):
        neighbour = words[i]

        while not neighbour.startswith(prefix):
            prefix = prefix[:len(prefix)-1]
            if prefix == "":
                return ""
        # end of while
    # end of for
    return prefix
# end of longestCommonPrefix()
```

### Code Explanation

asd

## Connected Readings

* **Functions (**[**Link**](../../defining-functions/functions.md)**)**
* **Type Hinting Functions (**[**Link**](https://docs.python.org/3/library/typing.html)**)**
* **List (**[**Link**](../../collections/tuples-and-lists/list-basics.md)**)**
* **Dictionary (**[**Link**](../../collections/dictionary.md)**)**
