# List Basics

**Lists** are a collection data item values.

* List is a built-in data type in Python 3
* Each item can be same or different data type (Int, Float, String, Boolean, List, and etc)
* Each items are separated by a comma except the last
* A list is denoted by square brackets: `[ ]`
* A list is iterable; therefore, we can traverse through it with a for loop
* Lists are compatible with the following built-in functions:
  * `str() and tuple()` :: can be converted to these data-types easily
  * `len()` :: returns the size of your list
  * `enumerate()` :: to help you pair index and items
  * `reversed()` :: will create a flipped iterator object
  * `sorted()` :: will help you return a sorted version of the list
  * `min() and max()` :: will help you determine the least and greatest value within a list, and compare lists
  * `sum()` :: in a list composed of numeric values, sum() will add up all the values
  * _many more, but they are deemed advanced and requires their own lessons_

**Examples:**

```python
# Examples of Lists in Python

a_list = [1,2,3,4,5,6]
b_list = ['h', 'e', 'l', 'l', 'o']
c_list = [
	[1,2,3,4,5,6],
	['h', 'e', 'l', 'l', 'o'],
	True
]

print('c_list:', c_list)
```

```
c_list: [[1, 2, 3, 4, 5, 6], ['h', 'e', 'l', 'l', 'o'], True]
```

#### Generating Lists from Sequences <a href="#generating-lists-from-sequences" id="generating-lists-from-sequences"></a>

**`list()` function:**

* Converts the argument into a list
* The argument should be either a sequence-like data (example: strings)

```python
# Using List()

result1 = list("hello")
result2 = list(range(10,20,3))
result3 = list(str(1234))

print('result1:', result1)
print('result2:', result2)
print('result3:', result3)
```

```
result1: ['h', 'e', 'l', 'l', 'o']
result2: [10, 13, 16, 19]
result3: ['1', '2', '3', '4']
```

#### Traversal & Accessing a List <a href="#traversal--accessing-a-list" id="traversal--accessing-a-list"></a>

**To Traverse:** _to travel across_; helps us get through our data.

```python
# For Loop & Lists

for item in [1,2,3,4, 'hello!']:
    print('Current item:', item)
```

```
Current item: 1
Current item: 2
Current item: 3
Current item: 4
Current item: hello!
```

**Lists are indexable**

Similar to strings, we can look at an individual value at an index location; returns a value.

```python
# List Indexing
# Format: list[location] gives us a value

a_list = [10, 13, 16, 19]
print('a_list[0]:', a_list[0])
print('a_list[1]:', a_list[1])
print('a_list[3]:', a_list[3])
print('a_list[-1]:', a_list[-1])
```

```
a_list[0]: 10
a_list[1]: 13
a_list[3]: 19
a_list[-1]: 19
```

We can also traverse by index:

```python
# List Traverse with index:

a_list = list('hello')

for i in range(len(a_list)):
    print('Item at index %d is %s.' % (i, a_list[i]))
```

```
Item at index 0 is h.
Item at index 1 is e.
Item at index 2 is l.
Item at index 3 is l.
Item at index 4 is o.
```

**Lists are Sliceable**

We can look at portions of a list by slicing; slicing returns a sample of the list back.

`Slicing = [start:end:step] step is 1 if not defined`

```python
# List Slicing

a_list = list(range(10,20))

print('a_list[0:len(a_list)]:', a_list[0:len(a_list)])
print('a_list[1:2]:', a_list[1:2])
print('a_list[:3]:', a_list[:3])
print('a_list[::-1]:', a_list[::-1])
print('a_list[-2:-4:-1]:', a_list[-2:-4:-1])
```

```
a_list[0:len(a_list)]: [10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
a_list[1:2]: [11]
a_list[:3]: [10, 11, 12]
a_list[::-1]: [19, 18, 17, 16, 15, 14, 13, 12, 11, 10]
a_list[-2:-4:-1]: [18, 17]
```
