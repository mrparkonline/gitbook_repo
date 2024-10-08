# Brute Force Algorithms

Brute force algorithms are straightforward methods for solving problems by trying all possible solutions until the correct one is found.&#x20;

They don’t use any shortcuts or optimizations, which often makes them simple to implement but inefficient for large datasets.

### Characteristics of Brute Force Algorithms:

* **Exhaustive Search:** They explore all possible solutions.&#x20;
* **Simplicity:** Easy to understand and implement.&#x20;
* **Inefficiency:** Can be slow and resource-intensive, especially for large inputs.&#x20;
* **Guaranteed Solution:** They will always find a solution if one exists, given enough time.&#x20;

### Example Brute Force Algorithms:

* [**Linear Search:**](../../03-complexity-and-algorithms/linear-search.md) Checking each element in a list sequentially.&#x20;
* [**Bubble Sort:**](../../03-complexity-and-algorithms/basic-sorting-algorithms.md) Repeatedly swapping adjacent elements if they are in the wrong order.
* **Password Cracking:** Trying all possible combinations until the correct one is found.

## Constructing a Brute Force Solution

### Sample Problem: Finding Factors of a Single Positive Integer

```python
def factors1(num : int) -> list:
    result = []
    for divider in range(1, num+1):
        if num % divider == 0:
            result.append(divider)
    return result
```

* The following program above is able to perfectly generate all the factors of a given positive integer.
* This algorithm is a brute force solution as it compares all numbers from 1 to the given number.
* If the given number was extremely large, the program would check all the numbers from 1 to the large number
* Therefore: `the performance of this algorithm is directly proportional` to the value of the input

#### Factoring Optimization

```python
def factors2(num: int) -> list:
    result = []
    end_point = int(num ** 0.5) + 1 # square root of our num
    
    for divider in range(1, end_point):
        quotient = num // divider
        remainder = num % divider
        if remainder == 0:
            result.append(divider)
            if quotient != divider:
                result.append(quotient)
    return result
```

* This function is an optimized version of our previous code where our algorithm stops at the square root of the number rather than the integer argument.
* The non-optimized factoring function is good because it is guaranteed to find an answer, but it will require more computation than necessary

| factors1(99980001)                                          | factors2(99980001)                                                                                   |
| ----------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| This function call will do 99,980,001 comparison operations | This function call will do square root of 99980001 comparison operations which is 9,999 comparisons. |
