# Pre-determined Arguments

We can set predetermined arguments when creating a functions to create versatility and complexity within our function.

### Example: Distance between two points or the origin <a href="#example-distance-between-two-points-or-the-origin" id="example-distance-between-two-points-or-the-origin"></a>

```python
def distance(x, y, a=0,b=0):
    ''' distance() calculates the distance between point(x,y) and point(a,b).
    If point(a,b) is not specified, it will calculate the distance from the origin to point(x,y)

    Distance Formula: https://www.khanacademy.org/math/geometry/hs-geo-analytic-geometry/hs-geo-distance-and-midpoints/v/distance-formula

    arguments:
    -- x : numeric
    -- y : numeric
    -- a : numeric
    -- b : numeric

    return
    -- distance in units
    '''

    delta_x = a - x
    delta_y = b - y

    result = (delta_x ** 2 + delta_y ** 2) ** 0.5

    return result
# end of distance()

print('Distance from (3,4) to (10,13) is %f units.' % distance(3, 4, 10, 13))
print('Distance from (5,12) from the origin is %f units.' % distance(5,12))
print('Distance from (1,1) to (5,5) is %f units' % distance(x=1, y=1, a=5, b=5))
```

```
Distance from (3,4) to (10,13) is 11.401754 units.
Distance from (5,12) from the origin is 13.000000 units.
Distance from (1,1) to (5,5) is 5.656854 units
```

**Explanation**

* Notice that when we first define the function, the last two arguments are assigned with values; This is called _predetermined arguments_
  * In a scenario when the user of the function doesn’t set these arguments, the function itself gives value to the missing arguments
* The predetermined arguments are changeable evidently by our first distance() function call
* We can also explicitly set each individual argument by the name of the arguments from the function (see the 3rd function call)

**Rules:**

1. The required arguments (arguments without predetermined values) must be defined first in the function
2. The predetermined arguments must be then defined after
