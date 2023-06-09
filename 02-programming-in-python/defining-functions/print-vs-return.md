# print() vs return

In this lesson we will be examining the differences between using a `print()` statement and a `return` statement

#### Example Function: Average of Integers in a List <a href="#example-function-average-of-integers-in-a-list" id="example-function-average-of-integers-in-a-list"></a>

```python
def averagePrint1(array):
    ''' averagePrint1() outputs the total average of all the integers in a list

    argument:
    -- array : a list of integers
    '''

    total_sum = sum(array)
    length = len(array)
    average = total_sum / length

    print('The average of the given list of values is:', average)
# end of averagePrint1

def averagePrint2(array):
    ''' averagePrint() returns the total average of all the integers in a list

    argument:
    -- array : a list of integers
    '''

    total_sum = sum(array)
    length = len(array)
    average = total_sum / length

    return average
# end of averagePrint2

# Start of the actual program

values = [96, 42, 55, 4, 12, 14, 67, 25, 37, 82, 62, 13]

print('Executing avereagePrint1():')
averagePrint1(values)
print('Executing avereagePrint2():')
averagePrint2(values)
print('-'*25)

print('Setting variables result1:')
result1 = averagePrint1(values)
print('Setting variables result2:')
result2 = averagePrint2(values)

print('-'*25)
print('Variable result1:', result1)
print('Variable result2:', result2)
```

```
Executing avereagePrint1():
The average of the given list of values is: 42.416666666666664
Executing avereagePrint2():
-------------------------
Setting variables result1:
The average of the given list of values is: 42.416666666666664
Setting variables result2:
-------------------------
Variable result1: None
Variable result2: 42.416666666666664
```

### `print()` vs `return` in our example <a href="#print-vs-return-in-our-example" id="print-vs-return-in-our-example"></a>

1. Calling the function without variable assignment:

When we first called `averagePrint1(values)`, it outputted the message with the result

When we first called `averagePrint2(values)`, it did not output anything

* This is the difference of using print() and return: print() outputs a message to the console whereas return does not

2. Assigning variables with the result of a function call:

When we output the variable `result1` the value is `None`.

When we output the variable `result2` the value is the resulting average.

* This happens because the function: **averagePrint1** does not return any value; therefore, variable **result1** cannot be assigned with the result from said function
* The function, **averagePrint2**, returns the **average** variable; therefore, it can be used for variable assignment

**NOTE:** 9 out of 10 times your functions should and will return a value
