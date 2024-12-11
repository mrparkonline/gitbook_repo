# Abstract Data Types

In computer science, an abstract data type (ADT) is a mathematical model for data types.&#x20;

An abstract data type is defined by its behavior (semantics) from the point of view of a user, of the data, specifically in terms of possible values, possible operations on data of this type, and the behavior of these operations.

## Stack

![](https://miro.medium.com/v2/resize:fit:1280/1\*lb-0r80YYhcnoVcQ3HY-1g.gif)

A stack is a **Last-In First-Out (LIFO)** abstract data structure

**Attributes:** A container that holds multiple data

**Methods:**

* `Push` → Adds Element to the top of the stack
* `Pop` → Removes the most recently added Element
* `Peek` → Look at the most recent element

Optional Methods:&#x20;

* **`size()`** -> Returns the number of items in the Stack
* **`isEmpty()`** -> Returns True if the stack is empty

### Stack & Complexity

All of stack operations are `O(1)` with Space complexity being `O(n)`.

### Stack Implementation in Python

```python
class Stack:
    def __init__(self):
        self.__storage = []
    
    @property
    def length(self):
        return self.size()
    
    def push(self, value):
        self.__storage.append(value)
    
    def pop(self):
        return self.__storage.pop()
    
    def peek(self):
        return self.__storage[-1]
    
    def size(self):
        return len(self.__storage)
    
    def isEmpty(self):
        return len(self.__storage) == 0
    
    def __str__(self):
        if self.isEmpty():
            return "<>"
        else:
            output = ", ".join(map(str, self.__storage))
            return f"<{output}>"
    
    def __repr__(self):
        return f"<Stack Object @{str(hex(id(self)))}>"
# end of Stack
```

