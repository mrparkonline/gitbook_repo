# String Slicing

In Python, you can also separate certain sections of the data if the date type is **slicable**.

Similar to indexing, we also use **\[ ] square brackets** to slice sequences.

#### Slicing Format <a href="#slicing-format" id="slicing-format"></a>

Given a string value, we can slice it as following:

```

string_value[starting_index : ending_index : step_value]

```

* **Slicing generates a new string**; therefore, slices can be set to a variable
* The slice will start and include the value at `starting_index`
* The slice will end at `ending_index`, but not include the value at the `ending_index`
* The `ending_index` can be a value greater than the largest index possible
* If the `step_value` is not specified, it is set to: `1`
* If the slicing values are set to an impossible outcome, it will return an empty string: `''`

```python
# Example
'''
Looking at: 'Hello!'

  |  H  |  e  |  l  |  l  |  o  |  !  |
  0     1     2     3     4     5     6

  |  H  |  e  |  l  |  l  |  o  |  !   
 -6    -5    -4    -3    -2    -1

'''

word = 'Hello!'

print('word:', word)
print('----------------------')
print('word[0:6]:', word[0:6])
print('word[0:5]:', word[0:5])
print('----------------------')
print('word[1:4]:', word[1:4])
print('word[:3]:', word[:3])
print('word[2:]:', word[2:])
print('word[:]:', word[:])
print('----------------------')
print('word[0:6:2]:', word[0:6:2])
print('word[::2]:', word[::2])
print('word[1:4:3]:', word[1:4:3])
print('word[::-1]:', word[::-1])
print('word[-5:-2]:', word[-5:-2])
print('word[6:0:-1]:', word[-5:-2])
print('word[-1:-6:-1]:', word[-1:-6:-1])
print('----------------------')
print('Some impossible slices and their results:')
print('word[6:0]:', word[6:0], '<< en empty string has been outputted.')
print('word[:20]:', word[:20], '<< There are no characters beyond the index of 6')
print('word[1:4:-1]', word[1:4:-1], '<< en empty string has been outputted.')
```

```
word: Hello!
----------------------
word[0:6]: Hello!
word[0:5]: Hello
----------------------
word[1:4]: ell
word[:3]: Hel
word[2:]: llo!
word[:]: Hello!
----------------------
word[0:6:2]: Hlo
word[::2]: Hlo
word[1:4:3]: e
word[::-1]: !olleH
word[-5:-2]: ell
word[6:0:-1]: ell
word[-1:-6:-1]: !olle
----------------------
Some impossible slices and their results:
word[6:0]:  << en empty string has been outputted.
word[:20]: Hello! << There are no characters beyond the index of 6
word[1:4:-1]  << en empty string has been outputted.
```

**Example:** Iterate through a string backwards

```python
# Example
# Looking at a string backwards through for loop

word = 'Hello World!'

for character in word[::-1]:
    print('Current Character:', character)
```

```
Current Character: !
Current Character: d
Current Character: l
Current Character: r
Current Character: o
Current Character: W
Current Character:  
Current Character: o
Current Character: l
Current Character: l
Current Character: e
Current Character: H
```
