# Nested Functions

Much like conditionals and iterations, we are allowed to have a _function inside a function_.

### Example: Factors of a Number in a List <a href="#example-factors-of-a-number-in-a-list" id="example-factors-of-a-number-in-a-list"></a>

```python
def factors(x):
    ''' factors() return a list of factors for x

    arguments:
    -- x : integer

    return
    -- list
    '''

    def isDivisible(num):
        ''' isDivisible() checks if given num is a factor of x'''

        return x % num == 0
    # end of inner function: isDivisible()


    result = []

    for i in range(1, x+1):
        if isDivisible(i):
            result.append(i)

    return result
# end of factors()

factors_12 = factors(12)
print('The factors of 12 are:', factors_12)

print('Is 12 divisible by 5?:', isDivisible(5)) # Should output an error
```

```
The factors of 12 are: [1, 2, 3, 4, 6, 12]



---------------------------------------------------------------------------

NameError                                 Traceback (most recent call last)

<ipython-input-2-08757aa984a8> in <module>
     28 print('The factors of 12 are:', factors_12)
     29
---> 30 print('Is 12 divisible by 5?:', isDivisible(5)) # Should output an error


NameError: name 'isDivisible' is not defined
```

There are a lot to unpack here.

1. We are allowed to define functions within a function
2. Functions defined within a function can only be called by the parent function (the top most function) this is called a **local scope**.
   * This is why we get an error when we try to call **isDivisible()** outside of the function
3. The **factors()** function uses its own **isDivisible()** function to check if a number is divisible by its own argument
   * Any variable or argument from the parent function is reference able by its own inner functions
   * This is why we can reference variable **x** inside **isDivisible()**
