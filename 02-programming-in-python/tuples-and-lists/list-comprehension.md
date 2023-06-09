# List Comprehension

**List Comprehension** is a concise method to create list in Python 3.

This technique is commonly used when:

* The list is a result of some operations applied to all its items
* It is a made from another sequence/iterable data
* The list is member of another list/sequence/iterable data that satisfies a certain condition

_This is where the **lambda function** would be used, but… we will learn the other way for readability._ _We will definitely talk about lambda functions in our Functional Programming Unit_

### List Comprehension Example 1 <a href="#list-comprehension-example-1" id="list-comprehension-example-1"></a>

We are to create a list which squares all the numbers from \[0,10)

```python
# Old Method
squares = []
for i in range(10):
    squares.append(i ** 2)

print('Our result: %s' % squares)
```

```
Our result: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

```python
# List Comprehension

squares = [i**2 for i in range(10)]

print('Our new result: %s' % squares)
```

```
Our new result: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

### How Does it Work? <a href="#how-does-it-work" id="how-does-it-work"></a>

List comprehension consists of:

* A **Square Bracket** containing an expression that describes the list
* One or more **For clause** to explain its members
* Then a zero or more **if clauses** depending on the complexity of the list

```
Examine: [i**2 for i in range(10)]

-- i**2 for i in range(10) --> is the expression that describe the list
-- i**2 describes each item in the list
-- i is taken from the for clause
-- for i in range(10) describes where i comes from
```

#### List Comprehension Example 2 <a href="#list-comprehension-example-2" id="list-comprehension-example-2"></a>

```
Create the list: [[1, 3], [1, 4], [2, 3], [2, 1], [2, 4], [3, 1], [3, 4]]
From
A = [1,2,3]
B = [3,1,4]

By using list comprehension
```

```python
# Solution
a = [1,2,3]
b = [3,1,4]

result = [[x, y] for x in a for y in b if x != y]
print(result)
```

```
[[1, 3], [1, 4], [2, 3], [2, 1], [2, 4], [3, 1], [3, 4]]
```

**Explanation:**

```
Each item of our list has to be a list of two values; therefore, each item is described as [x, y]

There are two for clauses because we are create a list from two sources
-- x comes from a
-- y comes from b

There is a condition to our item --> x != y
-- Therefore, as long as the condition x != y is true, we will add the item described as [x,y] to our resulting list
```

#### List Comprehension Example 3 <a href="#list-comprehension-example-3" id="list-comprehension-example-3"></a>

```
Use list comprehension to turn a 2D array called vec to a single list

vec = [[1,2,3], [4,5,6], [7,8,9]]
Output: [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

```python
# Solution

vec = [[1,2,3], [4,5,6], [7,8,9]]

result = [value for row in vec for value in row]
print('Vec as a single list of values: %s' % result)
```

```
Vec as a single list of values: [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

**Explanation**

```
Vec is an example of a matrix in Python 3 by using list of lists

To grab each value one by one from the rows we must do the following in order:
1. Explain what each item in the list comprehension is going to be ... in our case --> "value"
2. To now access where value is, define where it comes from ... in our case --> "row";
        therefore, for row in vec
3. Finally we construct our last for clause to denote that value comes from the row

With list comprehension, the order of your for clauses matter!
```
