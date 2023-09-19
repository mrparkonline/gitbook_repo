# String Formatting

## F-Strings

F-strings, or formatted string literals. _**This is the expected way to print strings in Python**_.

* Introduced in Python 3.6
* A concise and readable way to embed expressions inside strings.&#x20;
* F-strings are denoted by placing an 'f' character in front of a string literal and enclosing expressions within curly braces `{}`.

Here's a basic example of how to use f-strings in Python:

{% tabs %}
{% tab title="Example Code" %}
```python
name = "Alice"
age = 30

# Using an f-string to embed variables inside a string
message = f"Hello, my name is {name} and I am {age} years old."

print(message)
```
{% endtab %}

{% tab title="Output" %}
Terminal Output:

```
Hello, my name is Alice and I am 30 years old.m 30 years old.
```
{% endtab %}
{% endtabs %}

Here's a breakdown of how f-strings work:

1. Start the string with an 'f' or 'F' character before the opening quote.
2. Inside the string, you can enclose python expressions or variables within curly braces `{}`. These expressions will be evaluated and replaced with their values when the string is created.
3. You can include any valid Python expression inside the curly braces, not just simple variables. For example, you can perform calculations or call functions within the curly braces.
