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

The `__init__` special method, also known as a **Constructor**, is used to initialize the Car class with attributes such as `make`, `model`, and `year`.

In Python, built-in classes are named in lower case, but user-defined classes are named in CamelCase, with the first letter capitalized.

1. **Class Definition**: First, you define a class. Inside the class, you can declare attributes (variables) that belong to objects of that class.
2. **`__init__()` Method**: Within the class, you define the `__init__()` method. This method takes at least one argument, `self`, which is a reference to the object being created. It is a convention to name this parameter `self`, but you can technically choose any name. `self` allows you to access and modify the object's attributes within the method.
3. **Attribute Initialization**: Inside the `__init__()` method, you set the initial values for the object's attributes using `self`. These attributes can vary from one instance to another, so you can customize them during object creation.
4. **Object Creation**: When you create an instance of the class, the `__init__()` method is automatically called, and it initializes the attributes for that specific object.

```python
def __init__(self, make, model, year):
```

Our example `Car class` requires 3 arguments to create a car object: `make, model,` and `year`. We have these 3 arguments because we designed our class to have 3 **attributes**.

## Attributes

_Recall that:_ Attribute are the characteristics or qualities that an object of the class possesses as data of the object.

Attributes created in `.`**`init`**`()` are called **instance attributes**. An instance attribute’s value is specific to a particular instance of the class.

Our `Car class` has three instance attributes of `make, model,` and `year`. The `init()` method also has three arguments to help initialize the three attributes our class requires.

```python
# Car Attributes

car1 = Car("Tesla", "Model X", 2020)
print(f"Our car's make: {car1.make}.") # Expecting Output: "Our car's make: Tesla"
print(f"Our car's model: {car1.model}.") # Expecting Output: "Our car's model: Model X"
print(f"Our car's year of release: {car1.model}.") # Expecting Output: "ur car's year of release: 2020"
```

We can access an object's attribute by using the dot notation and the referencing the name of the attribute like the example provided above.

## Method vs Function

In Python, the key distinction between a method and a function lies in their association with objects. A function is a standalone block of code that takes input, performs operations, and returns a result.&#x20;

In contrast, a method is a function that is associated with an object and is called on that object. Methods are invoked using dot notation on instances of a class and typically operate on the data within that instance.

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

**For a class:**

* We can define what methods an object can use from the class. The definitiion is the same as creating a function, but you require one argument called `self`.
* The `car` class has two custom methods: `start_engine()` and `stop_engine()`
* The `car1` variable is a `Car` object; therefore, we can invoke/use the methods that the `Car` class has by using `a dot` then the `method name`. (Example: `car1.start_engine()`)

{% hint style="info" %}
In Python, `self` is a convention used to represent the instance of a class.&#x20;

It is the first parameter in the method definition of a class and refers to the instance of the class on which the method is invoked.&#x20;

When you call a method on an object, the object itself is passed as the first parameter to the method, and by convention, this parameter is named `self`.
{% endhint %}
