# Compare all possible prefixes

## Solution Breakdown

* Grab the first word of the dataset
  * We will be creating all possible for prefixes from this word
* Compare the rest of the dataset and see if the first word's prefixes can be a prefix from each word in the dataset
  * If so, return the longest prefix

### HOW-TO: Generating all prefixes from a string

```
Prefixes of the word flower:

"f"
"fl"
"flo"
"flow"
"flowe"
"flower"
```

#### Method 1: String concatenation with a loop

```python
word = "flower"
prefix = ""
for i in range(len(word)):
    prefix += word[i]
    print(f"Current Prefix: {prefix}")
```

#### Method 2: String slicing with a loop

```python
word = "flower"
prefix = ""
for i in range(1, len(word)+1):
    prefix = word[:i]
    print(f"Current Prefix: {prefix}")
```

### Pseudocode

```
# INSERT PSEUDOCODE HERE
```

## Python Solution

<pre class="language-python"><code class="lang-python">def longestCommonPrefix(words: list[str]) -> str:
<strong>    # If there is only 1 word in words, the word itself is a prefix
</strong>    if len(words) == 1:
        return words[0]
    
    initial_word = words[0]

    # Checking if the first word is an empty string
    if len(initial_word) == 0:
        return ""

    answer = ""
    prefix = ""

    # Step 1: Generate possible prefixes from initial_word
    for i in range(len(initial_word)):
        # Create prefix
        prefix += initial_word[i]

        # Step 2: Loop through the rest of the dataset and see if
        # each string starts with our current prefix
        is_prefix = False
        for j in range(1, len(strs)):
            current_word = words[j]

            if len(current_word) == 0:
                return ""
            elif current_word.startswith(prefix):
                is_prefix = True
            else:
                is_prefix = False
                return answer
        # end of inner for
        if is_prefix:
            answer = prefix
    # end of outer for
    return answer
# end of longestCommonPrefix()
</code></pre>

### Code Explanation

explanation

## Connected Readings

* Type Hinting Functions ([Link](https://docs.python.org/3/library/typing.html))
