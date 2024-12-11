# Arrays

{% embed url="https://www.youtube.com/watch?v=8hI1pUqsjwI" %}

Array is a data structure that allows you to store a collection of elements of the same data type.&#x20;

It provides a way to group multiple values under a single variable name, making it easier to manage and manipulate data.

### Array Format

```java
// Java Arrays:

dataType[] arrayName = new dataType[arraySize];
```

* Any datatype in java can create an array, we put empty square brackets after the datatype
* We provide a variable name for it
* We create a “new” array and we must set a size before we used it

### Examples of Arrays

```java
// integer array initialized
int[] numbers1 = new int[5]; // Line 1

// alterative way initialized
int numbers2[] = new int[5]; // Line 2

// Arrays set to values right away
int[] myArray = {1, 2, 3, 4, 5};

// A string array
String[] myArray1 = {"A", "B", "C", "D"};
```

* Implicit array **must have** its size (maximum number of items) declared. (Line 1 and 2)
  * This arrays currently have empty spots; they do not have values
* Use `{ ... }` to explicitly create an array.
* Explicit array (_arrays that already contain values_) do not need to specify the size.

### Array Requirements

1. The values in an Array must be all the same datatype
2. The number of total items in the Array must be set prior and it cannot be changed after&#x20;
3.  We can access individual items in a list by indexing,&#x20;

    `index value starts at zero (0)`
4. A value at a certain index can be changed which makes Arrays **mutable**.

## Mutability

Mutable means that the object has the ability to change without recreation.

An immutable data type can only be changed by having their variables reassigned to a new value.

{% hint style="info" %}
**Example:&#x20;**_**Strings are Immutable**_

`String name = "Jim";`

`name = "Tim"; // this is a valid code`

`name[0] = "J";`&#x20;

`// Only changing a single part of a String is impossible`
{% endhint %}

### Arrays are Mutable

When an array wants to change a value at a certain index, we do not need to recreate the array, but we can just update the value at the index.

```java
// Array Mutation Example
int[] numbers = {3,1,4,1,5,9};
numbers[2] = 9;
// numbers now contains --> {3,1,9,1,5,9}
// Value at index 2 got updated.
```

## Traversal: Way to look at each individual Values

{% tabs %}
{% tab title="Code" %}
```java
// While Loop Traversal of an Array

int[] nums = {3,1,4,1,5,9};

int i = 0;

while (i < nums.length) {
    System.out.println("nums at " + i + " is: " + nums[i]);
    i++; 
}
```
{% endtab %}

{% tab title="Output" %}
```
num at 0 is 3
num at 1 is 1
num at 2 is 4
num at 3 is 1
num at 4 is 5
num at 5 is 9
```
{% endtab %}
{% endtabs %}

**Explanation**

* All arrays have `.length` property to refer to the size of an array
* Indexing (_grabbing a value at a location)_ always starts at `0 zero`. It can be also said that the last item of an array is located at `length - 1` index.
* A similar traversal can be done with a for loop

```java
// Same Traversal with a for loop

int[] nums = {3,1,4,1,5,9};

for (int i = 0; i < nums.length; i++) {
    System.out.println("nums at " + i + " is: " + nums[i]);
}
```

## String Object to a Character Array

```java
// Example
String text = "Hello!"
char[] example = text.toCharArray()

// example now contains {'H', 'e', 'l', 'l', 'o', '!'}
```

In Java, `.toCharArray()` method converts the given string into a sequence of characters. The returned array length is equal to the length of the string.

## Character Array to String Object

```java
// Example

char[] example2 = {'W', 'o', 'r', 'l', 'd'}

String text2 = new String(example2);

// text2 is now "World"
```

By creating a new string similar to creating a new `scanner` and providing a Character Array as an input, you can create a new string.

## Printing an Array

_We cannot simply print an array within_ **`System.out.println()`**_. We must convert it to a_ **`string`** _first._

### Using `Arrays.toString()`

```java
// Example using Arrays.toString()

import java.util.Arrays; // 1. Import Your Arrays Library

class Main {
    public static void main(String[] args) {
        int[] nums = {3,1,4,1,5,9}; // Explicit integer array
        String str_nums = Arrays.toString(nums); // Converting int array to string
        
        String hello = "Hello, World!";
        char[] an_array = hello.toCharArray(); // converting hello to character array
        
        String str_array = Arrays.toString(an_array); // Making a printable char array
        
        System.out.println("Our nums: " + str_nums);
        System.out.println("Our char array: " + str_array); 
    }
}
```

**Output:**

```
Our nums: [3, 1, 4, 1, 5, 9]
Our char array: [H, e, l, l, o, ,,  , W, o, r, l, d, !]
```

## String to String Array using `.split()`

```java
// .split() --> Splitting a string based on a pattern
String digits = "1,2,3,4,5,6,7";
String[] converted = digits.split(",");
       
System.out.println(Arrays.toString(converted));
// converted now contains --> [1, 2, 3, 4, 5, 6, 7]
// Note that converted has string based digits ... "2" not integer 2

String word = "Apple Banana Cucumber";
String[] basket = word.split(" ");
System.out.println(Arrays.toString(basket));
// basket now contains --> [Apple, Banana, Cucumber]
```

Purpose of `.split()` is to locate separating patterns such as commas or whitespace in a string to obtain a collection of data.
