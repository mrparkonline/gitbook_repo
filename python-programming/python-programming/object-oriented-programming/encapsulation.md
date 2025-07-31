# Encapsulation

{% embed url="https://www.youtube.com/watch?v=MNeNk7L6QVg" %}

Encapsulation is related to a concept of **information hiding.** By following the practices of encapsulation, we can restrict the access to the classes/objects’ certain attributes and methods.

## Why Encapsulation?

Encapsulation's main purpose is to bundle data/attribute with the methods that operate on that data. Encapsulation is used to hide the values or state of a structured data object inside a class, preventing unauthorized parties’ direct access to them.

## Encapsulation within Custom Python Objects

To encapsulate attributes or methods in Python, we use the `__` prefix. (Double Underscoring)

```python
# Example
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.__mileage = 0 # mileage is encapsulated

    def start_engine(self):
        print(f"The {self.make} {self.model}'s engine is now running.")

    def stop_engine(self):
        print(f"The {self.make} {self.model}'s engine has been stopped.")
    
    def get_mileage(self):
        return self.__mileage
    
    def increase_mileage(self, amount):
        self.__mileage += amount
    
    def __reset_mileage(self): # reset_mileage() method is encapsulated
        self.__mileage = 0
# end of car class
```

If you examine the `Car` class, we have 1 new attribute and 3 new methods.

* Our new attribute: `mileage` is encapsulated. Therefore, we cannot access the value out side of the class definition.
* Since `mileage` is encapsulated, it is often a common practice to write a `getter` method to be able to grab hidden data. The method is designed to grab **encapsulated data** in a controlled and safe way. (Example: `get_mileage()`)
* When you want to design methods that you don't want objects to have access to, but you want your class definition to have access, you can also encapsulate methods with double underscoring as well. (Example: `__reset_mileage()`)

## Code from the Video Above

```python
'''
Goal: Encapsulation & Setter/Getter

Encapsulation --> Hiding Data / information hiding
-- Avoid methods and attributes to be accessed, changed, or even called outside of the class scope

Setter/Getter --> Controlling how programmers access attributes
-- Controlling to attribute behaviour

'''
# Member objects will have a name and an account number associated with them
class Member:
    def __init__(self, name, account_number):
        self._name = name
        self.__acc = self.__set_acc(account_number) # Encapsultion! hid this attribute
    
    # Name getter
    @property
    def name(self):
        return self._name

    # Name setter
    @name.setter
    def name(self, assigned_value):
        self._name = assigned_value.lower().replace(" ", '')

    @property # Getter for acc attribute
    def acc(self):
        return self.__acc

    def __set_acc(self, value):
        if isinstance(value, int):
            return value
        else:
            raise ValueError(f"{value} is not an integer.")

    def __str__(self):
        return f"{self.acc}: {self.name}"
# end of class Member

member1 = Member("Jasper Park", 1)
member1.name = "Mr. Park"
print(member1)
print(member1.acc)
```

## What are `getters` and `setters`?

{% hint style="danger" %}
**PLEASE DEFINE GETTERS BEFORE SETTERS**
{% endhint %}

### Getters

Getters retrieve value of a private attribute.

In Python, we use a decorator (use of @ symbol)

```python
@property # A decorator in python for getter methods
def name(self):
    return self._name
```

The following code snippet above is a getter for the attribute.

An object can now reference an attribute called `name` by invoking `.name` without the use of a method call with brackets like: `.name()`.

Creating a getter allows us to access variables that are encapsulated; moreover, you can create attributes that are read-only.

### Setters

Setters set or update a private attribute.

```python
@name.setter
def name(self, assigned_value):
    self._name = assigned_value.lower().replace(" ", '')
```

Setters are important because we get to control how an encapsulated can be changed.

The `name` attribute can still be updated by using the `=` operator; however, it will execute the setter we created above.
