# Inheritance & Overriding

## Inheritance

In object-oriented programming (OOP), inheritance is a mechanism that allows one class (called the subclass or derived class) to inherit the properties and behaviors of another class (called the superclass or base class). Inheritance is a key concept in OOP that facilitates code reuse and promotes the creation of a hierarchical structure for organizing and modeling software.

{% hint style="info" %}
“When I see a bird that walks like a duck and swims like a duck and quacks like a duck, I call that bird a duck.”

James Whitcomb Riley\
\
_It is not always required or even recommended to inheritance, unless you are 100% sure you are required to do so._
{% endhint %}

## Key Concepts of Inheritance

**Base Class (Superclass):** The class whose properties and behaviors are inherited by another class.

**Derived Class (Subclass):** The class that inherits from another class.

**Method Overriding:** The ability of a subclass to provide a specific implementation for a method that is already defined in its superclass.

**Code Reusability:** Inheritance promotes the reuse of code by allowing common functionality to be defined in a base class and shared among multiple subclasses.

**Hierarchy:** Inheritance enables the creation of a hierarchical structure of classes, where more specialized classes inherit from more general ones.

### Example Inheritance Code

```python
# Inheriting Vehicle
class Vehicle:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def display_info(self):
        print(f"{self.year} {self.make} {self.model}")

class Car(Vehicle):
    def __init__(self, make, model, year, num_doors):
        super().__init__(make, model, year)
        self.num_doors = num_doors

    def display_info(self):
        super().display_info()
        print(f"Number of doors: {self.num_doors}")

# Example usage
my_vehicle = Vehicle("Toyota", "Camry", 2022)
my_vehicle.display_info()

my_car = Car("Ford", "Mustang", 2023, 2)
my_car.display_info()
```

```
# Output
Toyota Camry 2022
Ford Mustang 2023
Number of doors: 2
```

* `Vehicle` is the base class with common attributes like make, model, and year, as well as a method `display_info` to display information about the vehicle.
* `Car` is a subclass of `Vehicle`. It inherits the attributes from `Vehicle` using `super().__init__(make, model, year)`, and it also has an additional attribute `num_doors` specific to cars. The `display_info` method is overridden to include information about the number of doors.

### `super()` method

{% hint style="info" %}
"Return a proxy object that delegates method calls to a parent or sibling class of type. This is useful for accessing inherited methods that have been overridden in a class."&#x20;

\- Python Documentation
{% endhint %}

`super()` in Python is a built-in function that is used to call a method from a parent class. It is often used in the context of inheritance to invoke a method or constructor from the parent class. This allows you to extend or override functionality in the child class while still reusing code from the parent class.

By using `super()`, you make your code more maintainable and allow for changes in the base class without having to update the derived classes manually.

In [**our example code**](inheritance-and-overriding.md#example-inheritance-code), `super().__init__(make, model, year)` is used to call the constructor (`__init__` method) of the parent class (`Vehicle`).&#x20;

This ensures that the `make`, `model`, and `year` attributes are initialized in the `Car` instance, leveraging the initialization logic from the `Vehicle` class.

## Overriding (Polymorphism)

Overriding occurs when two methods with the same method name and parameters within different classes. Overriding is a fundamental concept that shows polymorphism being evident in OOP.

**Here are some scenarios when overriding occurs.**

```python
class Vehicle:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def display_info(self):
        print(f"{self.year} {self.make} {self.model}")

class Car(Vehicle):
    def __init__(self, make, model, year, num_doors):
        super().__init__(make, model, year)
        self.num_doors = num_doors

    def display_info(self):
        super().display_info()
        print(f"Number of doors: {self.num_doors}")
```

There are two classes here:

1. A parent class called `Vehicle`
2. A child class called `Car`

{% hint style="info" %}
Both Classes have the methods: `display_info()`

The method has the same parameters

The method behaves differently in each class; therefore, _**the child class is overriding the behaviour from the parent class.**_
{% endhint %}

[**You can also override built-in magic-methods/built-in base methods from python standard library.**](override-magic-methods.md)
