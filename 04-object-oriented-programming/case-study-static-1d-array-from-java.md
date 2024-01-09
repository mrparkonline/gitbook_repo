# Case Study: Static 1D Array From Java

```python
class TypedArray:
    def __init__(self, dataType, size):
        self.__dataType = dataType
        self.__size = size
        self.__values = [None for _ in range(size)]
        self.__index = 0
    
    @property # dataType getter
    def dataType(self):
        return self.__dataType

    @property # size getter
    def size(self):
        return self.__size
    
    # __ 
    def __str__(self):
        return f"Array{self.dataType}[{self.size}] = " + str(self.__values)
    
    def __len__(self):
        return self.size
    
    def __getitem__(self, key):
        if not isinstance(key, int):
            raise TypeError(f"Key:{key} not an integer")
        elif key >= self.size or key < -self.size: 
            raise ValueError(f"Key:{key} out of bounds.")
        else:
            return self.__values[key]
    
    def __setitem__(self, key, new_value):
        if not isinstance(key, int):
            raise TypeError(f"Key:{key} not an integer")
        elif key >= self.size or key < -self.size: 
            raise ValueError(f"Key:{key} out of bounds.")
        elif not isinstance(new_value, self.dataType):
            raise TypeError(f"{new_value} is not {self.dataType}")
        else:
            self.__values[key] = new_value
    
    def __contains__(self, value):
        if not isinstance(value, self.dataType):
            return False
        else:
            for v in self.__values:
                if v == value:
                    return True   
            return False
    
    def __eq__(self, other_array):
        if self.size != other_array.size:
            return False
        elif self.dataType != other_array.dataType:
            return False
        else:
            for i in range(self.size):
                if self.__values[i] != other_array[i]:
                    return False
            else:
                return True
    
    # Making TypedArray Iterable
    def __iter__(self):
        return self
    
    def __next__(self):
        if self.__index >= self.size:
            self.__index = 0
            raise StopIteration
        else:
            value = self.__values[self.__index]
            self.__index += 1
            return value
    # end of Iterable

    #Custom Methods
    def toList(self):
        return self.__values
    
    # Polymorphism :o !!!
    def sort(self):
        self.__values.sort()
    
    def binarySearch(self, target):
        if not isinstance(target, self.dataType):
            raise TypeError(f"{target} is not {self.dataType}")
        else:
            self.sort()
            low = 0
            high = self.size - 1
            while (low <= high):
                mid = (low+high) // 2
                if self.__values[mid] == target:
                    return mid
                else:
                    if target > self.__values[mid]:
                        low = mid + 1
                    else:
                        high = mid - 1
            else:
                return -1   
# end of TypedArray
```

## Overview

`TypedArray()` is a Single Dimensional Container with a set size limit and limits the contents to be a single type.

## Attributes

```python
def __init__(self, dataType, size):
        self.__dataType = dataType
        self.__size = size
        self.__values = [None for _ in range(size)]
        self.__index = 0
```

To initialize our `TypedArray()`, we must specify the data type and set an integer max size for the array.

* At each index from `0 to (size-1)`, there is a `None` value to be place holders for incoming values
* The `None` values are stored in the encapsulated attribute called `.__values` as a list. Our goal is to not use any built-in methods related to list outside of the `class` definition
* The `.__index` attribute is used to make the array iterable

## Getters

```python
    @property # dataType getter
    def dataType(self):
        return self.__dataType

    @property # size getter
    def size(self):
        return self.__size
```

There are two read-only attributes: `.__datatype` and `.__size`. These two attributes were designed to be accessible at every scope.
