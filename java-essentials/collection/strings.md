# Strings

Strings are not technically part of the Collection set, but it behaves very similar. Consider String objects as a collection of characters.

## Joining Two Strings

Two strings can be joined by using the concatenation operator or method.

```java
// Using the operator
String first = "Mr. ";
String last = "Park";

String full_name = first + last;
System.out.println(full_name); // Outputs: Mr. Park

// Using the method
String a = "Hello";
String b = a.concat(" World!");

System.out.println(b); // Outputs: Hello World!
```

## Get Individual Characters from a String

String objects are composed of individual character primitive values; therefore, we can obtain individual characters from a string by using `charAt(index)`. Indexing starts at 0 for Strings.

```java
String fruit = "Strawberry";
char target = fruit.charAt(2);
System.out.println(target); // Outputs r
```

## Determine the number of characters in a String

`.length()` method is used to obtain the size of a string.

```java
String fruit = "Strawberry";
int size = fruit.length();
System.out.println(size); // Outputs 10
```

## Check a String's prefix or suffix

We can determine if a string starts with a certain pattern or if it ends with a certain pattern.

```java
String a = "Hello";
boolean start = a.startsWith("He");
boolean end = a.endsWith("lo!");

System.out.println(start + " " + end); // Outputs true false
```

## Replace a certain pattern in a String

We can search for a pattern within a String and replace all occurrence of it.

```java
String a = "Hello";
a = a.replace("ello", "i");
        
String b = "W O R L D";
b = b.replace(" ", "");
        
System.out.println(a + " " + b); // Outputs Hi WORLD
```
