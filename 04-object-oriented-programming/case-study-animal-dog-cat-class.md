# Case Study: Animal, Dog, Cat Class

```python
# Example

class Animal:
    def __init__(self, name):
        self._name = name  # Encapsulation: Using a protected attribute

    def make_sound(self):
        pass  # Abstract method, to be overridden by subclasses

    def get_name(self):
        return self._name

class Dog(Animal):
    def make_sound(self):
        return "Woof!"

class Cat(Animal):
    def make_sound(self):
        return "Meow!"

# Polymorphism: Using a common interface
def animal_sound(animal):
    return animal.make_sound()

# Creating instances of the classes
dog = Dog("Buddy")
cat = Cat("Whiskers")

# Accessing attributes through encapsulation
print(f"{dog.get_name()} says: {animal_sound(dog)}")
print(f"{cat.get_name()} says: {animal_sound(cat)}")

```
