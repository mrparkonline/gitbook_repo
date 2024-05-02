# ArrayList

{% embed url="https://www.youtube.com/watch?v=TZoIFgl-B4A" %}

An ArrayList in Java is a dynamic array that can hold elements of any data type.

Unlike a static array in Java, an **ArrayList can be resized dynamically.** This means that we can add and remove values from an ArrayList.

An ArrayList is a class in the `Java Collection` framework that is part of the `java.util` package

## Java ArrayList Requirements

1. **Import ArrayList from** `java.util`

```java
import java.util.ArrayList; // import the ArrayList class
```

2. Create an **ArrayList** object

```java
// Some code

import java.util.ArrayList; // import the ArrayList class

class Main {
    public static void main(String[] args) {
        ArrayList<String> cars = new ArrayList<String>();
        // Initializing the new arraylist about cars
    }
}
```

{% hint style="info" %}
The data type of the ArrayList's items must be **OBJECTS.** Moreover, they should be `Generic/Wrapper Class` **not primitive data types.**
{% endhint %}

| Primitive Data Type 👎 | Wrapper Class Equivalent 👍 |
| ---------------------- | --------------------------- |
| `int`                  | `Integer`                   |
| `double`               | `Double`                    |
| `boolean`              | `Boolean`                   |
| _does not exit_        | `String`                    |

_In Java, whenever we need data to be “objects” we have a Wrapper class to represent built-in data to be “objects”._

## Common ArrayList Methods

1. **Add an item to an ArrayList**

```java
// Add an item to an ArrayList

ArrayList<Integer> nums = new ArrayList<Integer>();
nums.add(3); nums.add(1); nums.add(4);
// nums is now composed of 3, 1, 4
```

We can use → .add() to add a value to an ArrayList to the END OF THE ARRAYLIST.

_What happens if you want to add a value at a certain index?_

```java
// Add an item to an ArrayList at a certain index
ArrayList<Integer> nums = new ArrayList<Integer>();
nums.add(3); nums.add(1); nums.add(4);

// nums is currrently: [3, 1, 4]
nums.add(3,1); // Adds 1 to the end of the list even though index is out of bounds; 
// The provided index can only be from [0, current length of arraylist] 
       
nums.add(0, 0); // Adds 0 to the front of the list, shifts everything back 
nums.add(2, 99); // Adds 99 at index 2; shifts everything from 2 onwards back by one.
        
//nums.add(100, 5); // Creates an error since the index is greater than the length.
System.out.println(nums); // Outputs: [0, 3, 99, 1, 4, 1]
```

**`.add(int index, value)`** can be also be used to add values to your ArrayList at certain locations following the rules/concepts below:

{% hint style="info" %}
**Rule A: Valid Index Range**

The index provided must be within the range of 0 to the size of the ArrayList (inclusive). If the index is outside this range, it will throw an `IndexOutOfBoundsException`.

**Rule B:. Shift Existing Elements**

When you add an element at a specific index, all elements at that index or greater are shifted one position to the right.

**Rule C. Capacity Check and Resize**&#x20;

If adding an element exceeds the current capacity of the ArrayList, it will automatically increase its capacity to accommodate the new element. This involves creating a new array with a larger capacity, copying the existing elements into the new array, and then adding the new element.

[_More reading on ArrayList Sizing_](https://www.geeksforgeeks.org/internal-working-of-arraylist-in-java/)
{% endhint %}

2. **Grab a value from an ArrayList**

```java
// Grabbing a Value

ArrayList<Integer> nums = new ArrayList<Integer>();
nums.add(3); nums.add(1); nums.add(4);

System.out.println(nums.get(0)); // prints 3
System.out.println(nums.get(2)); // prints 4
```

We can use → `.get(INDEX)` to grab value at a positive integer index value. (Index starts at zero always)&#x20;

_You can get an error if the index does not exist._

3. **Change a value at an index**

```java
// Change a value at a index

ArrayList<Integer> nums = new ArrayList<Integer>();
nums.add(3); nums.add(1); nums.add(4);

nums.set(0, 9);
// index of 0 has a value of 9 now
```

We can use → `.set(INDEX, NEWVALUE)` to change a value at a certain location.

4. **Remove a value at an index**

```java
// Remove a Value
ArrayList<Integer> nums = new ArrayList<Integer>();
nums.add(3); nums.add(1); nums.add(4);

nums.remove(2);
// nums ArrayLists now is only [3,1]
```

We can use → `.remove(INDEX)` to remove a value at a certain location.

5. **Get the size of the ArrayList**

```java
// Get Size of the ArrayList
ArrayList<Integer> nums = new ArrayList<Integer>();
nums.add(3); nums.add(1); nums.add(4);

System.out.println(nums.size()); // outputs: 3
```

We can use → `.size()` to determine the number of elements in an ArrayList.

6. **Check if a value exists in an ArrayList**

```java
// Does a value exist in an arraylist?
ArrayList<Integer> nums = new ArrayList<Integer>();
nums.add(3); nums.add(1); nums.add(4);

System.out.println(nums.contains(1)); // outputs: true; 1 exists in nums
System.out.println(nums.contains(10)); // outputs: false; 10 does not exist in nums
```

We can use → `.contains()` to determine if a value exists in an ArrayList.

7. **Determine the index of a value in an ArrayList**

```java
// Does a value exist in an arraylist?
ArrayList<Integer> nums = new ArrayList<Integer>();
nums.add(3); nums.add(1); nums.add(4); nums.add(1); nums.add(5); nums.add(9);

System.out.println(nums.indexOf(4)); // Returns 2 (4 is at index 2)
System.out.println(nums.indexOf(1)); // Returns 1 (The first location of 1)
System.out.println(nums.indexOf(10)); // Returns -1 (10 DNE)
System.out.println(nums.lastIndexOf(1)); // Returns 3 (Last occurrence of 1)
```

We can use → `.indexOf()` to determine an index of a value in an ArrayList. Returns -1 if not found.

We can use → `.lastIndexOf()` to determine an index of a value in an ArrayList from the right. Returns -1 if not found.

## ArrayLists are printable!

```java
// Example

ArrayList<String> cars = new ArrayList<String>();

cars.add("Honda");
cars.add("Toyota");
cars.add("Mercedes");
cars.add("Ford");

System.out.println("Our car brands: " + cars);
```

**Output:**

```
Our car brands: [Honda, Toyota, Mercedes, Ford]
```

As long as the ArrayList contains primitive equivalent wrapper class items, we can simply print the ArrayList within **`System.out.println()`**.
