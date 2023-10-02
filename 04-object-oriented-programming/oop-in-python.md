# OOP in Python

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
```

The example above is a class called "Car".

* Within a `class` code block, we write all codes that would belong to the class.

