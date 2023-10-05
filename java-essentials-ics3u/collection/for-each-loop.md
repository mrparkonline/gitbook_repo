# For Each Loop

In Java, you can use a for-each loop, also known as an enhanced for loop, to iterate over elements of an iterable collection or array without explicitly controlling the iteration variables.&#x20;

This loop simplifies the process of iterating through collections and arrays.

## Traversing a String

In Java, you cannot use a for-each loop (enhanced for loop) to directly traverse each character of a string because a string is not considered an iterable collection like arrays.

```java
String str = "Hello, World!";
char[] charArray = str.toCharArray();

for (char ch : charArray) {
    System.out.println(ch);
}
```

```
// Output:
H 
e 
l 
l 
o 
, 
  
W 
o 
r 
l
d
!
```

### Explanation

1. We first convert the string `str` into a character array using the `toCharArray()` method, which splits the string into individual characters.
2. Then, we use a for-each loop to iterate over the characters in the `charArray`.
3. We have now printed each individual characters of the string

## Traversing an Array

```java
double[] numbers = { 1.2, 2.3, 3.4, 4.5, 5.6 };

// Use a for-each loop to traverse the array
for (double num : numbers) {
    System.out.println(num);
}
```

```
// Output
1.2
2.3
3.4
4.5
5.6
```

### Explanation

1. We define an array of doubles named `numbers`.
2. We use a for-each loop to iterate over each element in the `numbers` array.
3. The loop variable `num` takes on the value of each element in the array one by one, allowing you to perform operations or print the values as needed.

