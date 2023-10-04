# OOP in Python

## Object Oriented Programming

1. A defined class will have its own attributes and methods
2. An object can be created after a class is defined
3. Attributes are data that belong to an object
4. Methods are actionable code that the object can do

## `class` Keyword

```python
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def start_engine(self):
        print(f"The {self.make} {self.model}'s engine is now running.")

    def stop_engine(self):
        print(f"The {self.make} {self.model}'s engine has been stopped.")
# end of class

# global programming flow:
car1 = Car("Tesla", "Model X", 2020) # we must provide 3 required arguments to create a Car

car1.start_engine() # self is not a required argument, rather it is always assumed to be there.
# car1 can now use the method "start_engine()" since it is a Car object

```

The example above is a class called "Car".

* Within a `class` code block, we write all codes that would belong to the class.
* `class` must be assigned a name, it follows the same name conventions as variables except that the name must be **capitalized.**
* `__init(self)__` is an "initialization" method that auto runs when we create an object from a class.

### `__init__(self)` The initialization method

1. **Class Definition**: First, you define a class. Inside the class, you can declare attributes (variables) that belong to objects of that class.
2. **`__init__()` Method**: Within the class, you define the `__init__()` method. This method takes at least one argument, `self`, which is a reference to the object being created. It is a convention to name this parameter `self`, but you can technically choose any name. `self` allows you to access and modify the object's attributes within the method.
3. **Attribute Initialization**: Inside the `__init__()` method, you set the initial values for the object's attributes using `self`. These attributes can vary from one instance to another, so you can customize them during object creation.
4. **Object Creation**: When you create an instance of the class, the `__init__()` method is automatically called, and it initializes the attributes for that specific object.

```python
def __init__(self, make, model, year):
```

Our example `car class` requires 3 arguments to create a car object: `make, model,` and `year`.

