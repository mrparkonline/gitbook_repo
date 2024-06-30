# String Indexing

In Python, we can access a certain/individual item in a sequence if the data type is **indexable**.

To index/access a single item from a string, we use **\[ ] square brackets**.

```python
# Example
'''
Looking at: 'Hello!'

 |  H  |  e  |  l  |  l  |  o  |  !  |
 0     1     2     3     4     5     6

'''

word = 'Hello!'

print('word[2]:', word[2])
print('word[1]:', word[1])
print('word[0]:', word[0])
print('word[5]:', word[5])
print('word[6]:', word[6])
```

```
word[2]: l
word[1]: e
word[0]: H
word[5]: !



---------------------------------------------------------------------------

IndexError                                Traceback (most recent call last)

<ipython-input-3-f291ab6028d1> in <module>
     14 print('word[0]:', word[0])
     15 print('word[5]:', word[5])
---> 16 print('word[6]:', word[6])


IndexError: string index out of range
```

**NOTE:**

* Indexing always **starts at 0 (zero)**
* Indexing always accesses a single item from the sequence, for strings: **a character from the targetted string**
* The index value _cannot go beyond the limit of the sequence_. Mathematically, the index value cannot be greater than length of the sequence subtracted by one.
  * Examine the error for `print('word[6]:', word[6])`: gives us index out of range error

```
Looking at: 'Hello!'

 |  H  |  e  |  l  |  l  |  o  |  !  |
 0     1     2     3     4     5     6

```

* Notice that our index value in this diagram starts at the **left of the item**
* When we index, it will go to the given location and look at the item to the right of the index
  * Therefore, `print('word[1]:', word[1])` gives us: `e`

#### Negative Indexing <a href="#negative-indexing" id="negative-indexing"></a>

Just like how we can use positive integer-indexes to access values, we can also use negative integer-indexes to access values as well.

```python
# Example
'''
Looking at: 'Hello!'

 |  H  |  e  |  l  |  l  |  o  |  !  |  H  |  e  |  l  |  l  |  o  |  !  |
-6    -5    -4    -3    -2    -1     0     1     2     3     4     5     

'''

word = 'Hello!'

print('word[-1]:', word[-1])
print('word[-3]:', word[-3])
print('word[-5]:', word[-5])
print('word[-6]:', word[-6])
print('word[-7]:', word[-7])
```

```
word[-1]: !
word[-3]: l
word[-5]: e
word[-6]: H



---------------------------------------------------------------------------

IndexError                                Traceback (most recent call last)

<ipython-input-6-5d7a5ddd18cd> in <module>
     14 print('word[-5]:', word[-5])
     15 print('word[-6]:', word[-6])
---> 16 print('word[-7]:', word[-7])


IndexError: string index out of range
```

**NOTE:**

* Index of `-1` is the quickest way to grab the last value of an indexable sequence
* Examine that at -6 and 0 we got the value of `H` for `Hello!`, they are located at the same place

```
Looking at: 'Hello!'

 |  H  |  e  |  l  |  l  |  o  |  !   
-6    -5    -4    -3    -2    -1      

```

* Much like how we look at the right of positive indexes, we do the same for negative indexes
* The indexes are laid out like an integer line with the string itself duplicated; however, Python does not actually create the string as a double
  * It is **smart enough** to know how to handle positive and negative indexes with a single instance of the sequence
