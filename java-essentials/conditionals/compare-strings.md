# Compare Strings

To compare the equalities of strings, Java provides various methods to help us do so.

### Using `.equals()`

```java
String myStr1 = "Hello";
String myStr2 = "Hello";
String myStr3 = "Another String";
System.out.println(myStr1.equals(myStr2)); // Returns true because they are equal
System.out.println(myStr1.equals(myStr3)); // false
```

In Java, the `.equals()` method is used to compare the contents (values) of two strings to determine if they are equal.&#x20;

When you use `.equals()` to compare strings, it checks whether the character sequences within the two string objects are identical.&#x20;

This means that if the characters in both strings are the same and appear in the same order, the `.equals()` method returns `true`, indicating that the strings are equal; otherwise, it returns `false`.

### Using `.comparesTo()`

```java
String myStr1 = "Hello";
String myStr2 = "Hello";
System.out.println(myStr1.compareTo(myStr2)); // Returns 0 because they are equal
```

In Java, the `.compareTo()` method is used to compare strings lexicographically (i.e., in dictionary order) to determine their relative ordering.&#x20;

This method is available in the `java.lang.String` class and returns an integer value that indicates the comparison result.&#x20;

The `.compareTo()` method has the following signature:

```java
int compareTo(String anotherString)
```

* It takes another string (`anotherString`) as its argument.
* It returns an integer value, which can have one of three possible outcomes:
  * If the calling string (the one on which `.compareTo()` is invoked) is lexicographically less than the `anotherString`, it returns a negative integer.
  * If the calling string is lexicographically greater than the `anotherString`, it returns a positive integer.
  * If the calling string and `anotherString` are lexicographically equal, it returns `0`.

### Lexicographic Ordering:

* "apple" comes before "banana" because 'a' comes before 'b' in the Unicode character set.
* "apple" comes after "app" because 'l' comes after 'p,' and the length of "apple" is greater than "app."
* "Apple" comes before "apple" because 'A' comes before 'a' in the Unicode character set.
* "apple" comes before "Applesauce" because "apple" is shorter and is a prefix of "Applesauce."
