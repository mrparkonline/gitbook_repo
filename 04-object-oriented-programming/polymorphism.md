# Polymorphism

Polymorphism is a fundamental concept in object-oriented programming (OOP) that allows objects of different types to be treated as objects of a common base type. The term "polymorphism" comes from the Greek words "poly," meaning many, and "morph," meaning form. There are two main types of polymorphism: compile-time (or static) polymorphism and runtime (or dynamic) polymorphism.

_Same attribute names existing in multiple classes is not polymorphism._

**When dealing with polymorphism, we often just analyze methods.**

{% hint style="info" %}
One type of Polymorphism called **`Overloading`** is not a concept that is available in Python.\
\
[More info here.](https://www.pluralsight.com/guides/overload-methods-invoking-overload-methods-csharp)
{% endhint %}

The two main types of polymorphism in Python is:

1. Different Classes, Same Named Methods, but different behaviour.
2. [**Overriding** & **Inheritance**](inheritance-and-overriding.md) **(Next Page)**

## Basic Method Polymorphism

```python
# Polymorphism Example

class Dog:
    def sound(self):
        print("Bark!")

class Cat:
    def sound(self):
        print("Meow~")
        
class Bird:
    def sound(self):
        print("Peep.")
```

If we examine the 3 simple classes we made of `Dog`, `Cat`, and `Bird`, they all share a common method called `sound()`.&#x20;

However, the behaviour of the method is different as a dog barks, a cat meows, and a bird peeps.&#x20;

Methods showing polymorphism can differ by their arguments of the method and/or by their output/returned value of the method.
