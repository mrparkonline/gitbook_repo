# Functions

{% embed url="https://www.youtube.com/watch?v=u-OmVr_fT4s" %}

* In Python 3, we are able to create custom functions that are much similar to the built-in functions we have encountered
* These functions are callable and can output results to our liking
* This allows us to organize our code when our projects become more complex
* In this unit we will only cover introductory level content for functions (returning values, predetermined arguments, and nested functions).

### What is a Function? <a href="#what-is-a-function" id="what-is-a-function"></a>

**Function:** a block of organized, reusable code that is usually used to perform single and related action.

_Similar concepts: methods, subroutines and procedures_

**Mathematical Functions vs Programming Functions**

**Mathematical Function:** Functions we learn in math classes, such as Grade 11 Functions, are by in nature following the laws of mathematics. These functions (Quadratic, Rational, Trignometric and Logarithmic to name a few) are all about relating an input to an output. They also must follow the these rules:

1. One input must have only one output
2. Multiple inputs are allowed to have same output

**Programming Function:** In computer science, a function is a self contained module of code. It is not restricted to the rules of mathematical function _unless you want it do be_.

### Mindset for writing Functions in Python <a href="#mindset-for-writing-functions-in-python" id="mindset-for-writing-functions-in-python"></a>

1. **Clean Code:** We want organize a solution to problem or a part of a problem into a single function
2. **Algorithms:** Without functions, we cannot express algorithms properly
3. **Reusability:** Functions prevent us from repeating code you’ve written before
4. **Single Serving:** Functions prevent overloaded programs that look like spaghetti

### Python Function Syntax <a href="#python-function-syntax" id="python-function-syntax"></a>

```python
def functionName(arg1, arg2, arg3):
    # docStrings for a function is created with triple-quotation marks
    ''' short + sweet single line explanation of what the function does
    
    Args:
        arg1: description, mention datatype
        arg2: description, mention datatype
        arg3: description, mention datatype
    
    Returns:
        the datatype of the returned object, describe what it represents too
    '''

    # write code inside the function here

    return value
# end of functionName()
```

**How to use docstrings**&#x20;

1. Write a short single sentence on what the function does
2. List each arguments and describe what they are and the datatype
3. Describe the return statements data type and what it returned.

{% hint style="info" %}
A docstring should give enough information to write a call to the function without reading the function’s code. The docstring should describe the function’s calling syntax and its semantics, but generally not its implementation details, unless those details are relevant to how the function is to be used. ([**Source**](https://google.github.io/styleguide/pyguide.html#383-functions-and-methods))
{% endhint %}

**Function Rules:**

* `def` is the keyword designated to help us **define** a custom function
* a function must have a callable name … it is recommended to use name that is not [built-in function](https://docs.python.org/3/library/functions.html) or [keywords](https://www.tutorialspoint.com/What-are-Reserved-Keywords-in-Python) for Python.
* `(arg1, arg2, arg3):` This is state our function inputs. The number of inputs a function require is up to you. A proper definition for function inputs are called **arguments**.
* We can also write a descriptor for our function by using triple single(') or double(") quotation marks
* `return` is a keyword designed for functions. When a function is done executing its code, we can use **return** to help us grab the result of our function

**Let’s create an example function for the area of a circle.**

```python
def areaCircle(radius, pi=3.14):
    ''' calculates the area of a circle

    arguments:
        radius : represents the radius value of a circle, floating point value
        pi : takes in a pi value, assumed to be 3.14 if not provided, floating point value

    return:
        an integer describing the caluculated area
    '''

    area = pi * (radius ** 2)

    return area
# end of areaCircle

my_radius = 6
pi = 3.14159

my_circle_area = areaCircle(my_radius, pi)
my_circle_area2 = areaCircle(my_radius, 3.14)

print(f'The area of my circle is {my_circle_area} units squared.')
print(f'The area of my circle with pi of 3.14 is {my_circle_area2} units squared.')
```

```
The area of my circle is 113.0972 units squared.
The area of my circle with pi of 3.14 is 113.0400 units squared.
```

### Explanation <a href="#explanation" id="explanation"></a>

1. We defined a function called _areaCircle_
2. There are 2 arguments
   * radius
   * pi
3. There is a docstring trapped inside triple single quotation marks
4. Variable area inside the function is calculated by using the argument variables for the function
5. We use the **return** keyword to help us grab the resulting variable called: _area_
6. After the function has been defined we created our new variables of **my\_radius** and **pi**
   * please note that the new variable pi = 3.14159 does not conflict with the function’s argument variable
   * We can use these new variables to be the explicit arguments for when we call the function
7. We calculated the result for two variables: **my\_circle\_area** and **my\_circle\_area2** by assigning it to the result of us calling our defined function
   * When the function **areaCircle** is called, it will take the given arguments to calculate the function’s area variable
   * Once the calculation is finished, it will be **returned** back to the variable and assigned with the result
