# 🍎 Python Basics

This section of the book will cover the basic skills to create variables, obtain keyboard inputs through the console, output data to the console, and do mathematical calculations.

## Major Definitions

* **Variable**: A container that holds data for a program.
* **Function:** A built-in or custom segment of executable code.
* **Comment:** Human readable notes written by a programmer for others to read. Often used to describe certain aspects of the code.

Whenever we name a variable or a function we create an **Identifier**.

{% hint style="info" %}
_Rules for Identifiers:_

* Cannot use [**Keywords**](https://www.w3schools.com/python/python_ref_keywords.asp) as identifier names&#x20;
* No punctuation characters&#x20;
* An identifier should always start with letters (A-Za-z) then followed by alphanumeric characters ... _an identifier cannot start with numbers (0-9)_
{% endhint %}

### Identifier Naming Conventions

1. You don’t start a variable with capitals
2. There are no white spaces, we connect multi word variables with either camelCasing or under\_scores.
3. Variable names should be effective and short, not vague.

**Example of a Python Code using an Identifier**

```python
# Our First Line of Python Code
user_name = "Jane Doe"
print(user_name)
```

1. `# Our First Line of Python Code` is an example of a `comment`. The `#` symbol creates a single line comment.
2. `user_name = "Jane Doe"` is an example of a `variable` containing the data `"Jane Doe"`; it is using the `under_score` naming convention
3. `print(user_name)` is an example of using a function to output a value to the [**console**](https://www.digitalocean.com/community/tutorials/how-to-work-with-the-python-interactive-console).

