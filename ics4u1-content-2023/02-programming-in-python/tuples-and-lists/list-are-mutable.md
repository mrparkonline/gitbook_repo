# List are Mutable

Lists are mutable data type. This means that its composition can be altered without recreation, reassignment, redeclaration. This can be dangerous for most new programmers.

**Example 1: Altering via index:**

```python
# Manipulation by index

primes = [2,3,5,7,11]
print('primes currently:', primes)
primes[1] = 10000
primes[2] = 'Hello!'

print('primes now:', primes)
```

```
primes currently: [2, 3, 5, 7, 11]
primes now: [2, 10000, 'Hello!', 7, 11]
```

In example 1, you can see that we can change the composition of the list without redeclaring a new list for the variable: `primes`.

**Example 2: Copying a List to another variable:**

```python
# Copying a list to a new variable

primes1 = [2,3,5,7,11]
primes2 = primes1
print('primes1 currently:', primes1)
print('primes2 currently:', primes2)

primes2[-1] = 13

print('primes1 now:', primes1)
print('primes2 now:', primes2)
```

```
primes1 currently: [2, 3, 5, 7, 11]
primes2 currently: [2, 3, 5, 7, 11]
primes1 now: [2, 3, 5, 7, 13]
primes2 now: [2, 3, 5, 7, 13]
```

In example 2, we have only manipulated the list called `primes2`. However, the original list called `primes1` was also affected by the changes as well.

This is because when a new variable is created to hold another list variable. Python saves memory by pointing towards where the original list is located rather than creating a whole new copy.

Therefore, any changes will affect both variables.

**Solution:** Use a method called `.copy()`

This method will help us create a new list in memory with the same values from the original.

```python
# Using .copy() method

primes1 = [2,3,5,7,11]
primes2 = primes1.copy()
print('primes1 currently:', primes1)
print('primes2 currently:', primes2)

primes2[-1] = 13

print('primes1 now:', primes1)
print('primes2 now:', primes2)
```

```
primes1 currently: [2, 3, 5, 7, 11]
primes2 currently: [2, 3, 5, 7, 11]
primes1 now: [2, 3, 5, 7, 11]
primes2 now: [2, 3, 5, 7, 13]
```

**Example 3: Sorting & List Methods**

List has a built-in method to help sort. Unlike the `sorted()` function, list has a method which allows us to manipulate the list you are sorting without creating a whole new variable.

```python
# List. sort() method

a_list = list('Hello, World!')
print('a_list now:', a_list)

a_list.sort()

print('a_list sorted:', a_list)
```

```
a_list now: ['H', 'e', 'l', 'l', 'o', ',', ' ', 'W', 'o', 'r', 'l', 'd', '!']
a_list sorted: [' ', '!', ',', 'H', 'W', 'd', 'e', 'l', 'l', 'l', 'o', 'o', 'r']
```

Examine that there is no **assignment operation** occurring to help us sort. We are using a method that lists have to just manipulate the given list rather than needing to create a new container _like strings._

Below are the list of methods that affect the composition of a list. They will not require recreation/reassignment.

* append()
* extend()
* insert()
* remove()
* pop()
* sort()
* reverse()
