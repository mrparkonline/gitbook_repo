# Override Magic Methods

## Making Objects Printable

```python
class Employee: 
    def __init__(self, name, age, id): 
        self.name = name 
        self.age = age
        self.id = id 

employeeObject = Employee('employeeName', 20, 1101)

print(employeeObject)
```

Outputs

```
<__main__.Employee object at 0x000001DBB695FB50>
```

This occurs because we did not code a behaviour for our objects when they are used in _**String Scenarios.**_** We must override two functions:** [**`str()`**](https://docs.python.org/3/library/functions.html#func-str) **and** [**`repr()`**](https://docs.python.org/3/library/functions.html#repr)**.**

{% hint style="info" %}
To make an object printable.

We must override two built-in base functions in Python:

1. `__str__()`
2. `__repr__()`
{% endhint %}

The **`__str__()`** method returns a human-readable, or informal, string representation of an object. Often called when the object is within a `print()` or `str()`

The **`__repr__()`** method returns a more information-rich, or official, string representation of an object. This is often called when your custom object needs to be displayed within another or any other sitution where `__str__()` is not used.

### Fix

```python
class Employee: 
    def __init__(self, name, age, id): 
        self.name = name 
        self.age = age
        self.id = id 
    
    def __str__(self):
        return f"{self.id}: {self.name}"
    
    def __repr__(self):
        return f'Employee(name = {self.name}, age = {self.age}, id = {self.id})'

employeeObject = Employee('employeeName', 20, 1101)

print(employeeObject)
print(repr(employeeObject))
```

Outputs:

```
1101: employeeName
Employee(name = employeeName, age = 20, id = 1101)
```

## Other Base Functions to Override.

TBC
