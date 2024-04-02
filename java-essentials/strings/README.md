# Strings

**`String`** is a collection of **Characters** represented in Java.

`Characters` is a primitive datatype in Java that represents single [**ASCII**](https://en.wikipedia.org/wiki/ASCII#Printable\_characters) characters trapped within single quotation marks.

```java
// Characters Examples
char myGrade = 'B';
char myVar1 = 65; // Contains A 
myVar2 = 66; // Contains B
myVar3 = 67; // Contains C
```

**`String`** is a built-in class in Java where we can create `String` objects. Objects will also have methods which provides access to `String` class features.

### Indexing a String

Indexing a String is a concept of getting a singular character from the String. Always remember that indexing starts at `0`.

```java
/*
Looking at: "Hello!"

 Word  --> |  H  |  e  |  l  |  l  |  o  |  !  |
 Index --> 0     1     2     3     4     5     

*/

String word = "Hello!";
char last = word.charAt(5); // last contains !
char first = word.charAt(0); // first contains H
```

### Size of a String

Since we can access individual characters by accessing the index, it is often nice to know the length/size of a String.

```java
String word = "Hello!";
int word_size = word.length(); // Contains 6
```

### Finding a Character or a Pattern

When you don't know the index of a character or a certain pattern within the String, you can use a `indexOf()` method to find the index.

```java
String word = "Hello!"
int index1 = word.indexOf('l'); // index1 will be 2
int index2 = word.indexOf("lo"); // index2 will be 3
```

### Lowercase and Uppercase String

You can convert a `String` to have all its characters be either lowercase or uppercase.

```java
// Lowercase
String word1 = "HELLO!!";
word1 = word1.toLowerCase(); // word1 is now hello!

// Uppercase
String word2 = "goodBye!";
word2 = word2.toUpperCase(); // word2 is now GOODBYE!
```
