# Handling User Inputs & Type Conversion

## Using the `.nextLine()` method

The `.nextLine()` method in Java's Scanner class is used to read a line of text from the input source (usually the keyboard or a file) and return it as a String.&#x20;

It reads the text until it encounters a newline character ( '\n' ) or the end of the input, and then it consumes the newline character.

Here's a simple example of how to use `.nextLine()` to read a line of text from the console:

```java
// Example Program
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter a line of text: ");
        String inputLine = sc.nextLine();

        System.out.println("You entered: " + inputLine);

        sc.close();
    }
}
```

In this example, the program prompts the user to enter a line of text, and when they press Enter, `.nextLine()` reads that entire line as a String and stores it in the `inputLine` variable.&#x20;

You can then use the `inputLine` variable to work with the user's input.

### Closing your `Scanner` object

1. **Resource Management:**&#x20;

When you create a Scanner object to read from a source like `System.in` (the keyboard), it establishes a connection to that source and allocates system resources.&#x20;

If you don't close the Scanner, these resources may not be released properly, which can lead to resource leaks and potential issues.

2. **Input Stream Cleanup:**&#x20;

Closing the Scanner not only releases resources but also signals to the underlying input stream (e.g., `System.in`) that you are done reading from it.&#x20;

This is important because leaving the input stream open can cause unexpected behavior in your program, especially when reading from multiple sources.

In the context of the code sample:

```java
Scanner scanner = new Scanner(System.in);
// ...
scanner.close();
```

Closing the `scanner` object at the end ensures that any resources associated with it are properly released, and it signals that you've finished reading from the standard input, preventing any potential issues or interference with future input operations in your program.

So, always remember to close your Scanner or any other resource-handling objects when you are done with them to maintain proper resource management and prevent unexpected behavior.

## Type Conversion

Since `.nextLine()` method only reads keyboard input as a String, we need a way to convert a value to an integer or double if we need to do arithmetic. We also need a way to convert it back to String if needed.

```java
// Example: Adding two inputted values
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("Enter a number:");
        String input1 = sc.nextLine();
        int num1 = Integer.parseInt(input1); // String --> Integer
        
        System.out.println("Enter another number:");
        String input2 = sc.nextLine();
        int num2 = Integer.parseInt(input2); // String --> Integer
        
        int result = num1 + num2;
        String answer = Integer.toString(result); // Integer --> String
        System.out.println("The sum is: " + answer);
    }
}
```

### `Integer.parseInt(String obj)`

By using a method from the `Integer` class, we can convert a string object to an integer.&#x20;

The rule is that the argument[^1] must have proper integer like values. For example, we cannot convert a word to an integer.

### `Integer.toString(int obj)`

Similar to how we can convert a String object to an integer, we can do the reverse.

#### Other Type Conversion Methods:

1. `Double.parseDouble(String obj)` --> converts a String to double
2. `Double.toString(double obj)` --> converts a double to String
3. Boolean.parseBoolean(String obj) --> converts a String to Boolean (only `"true"` turns to `true` all else is `false`)
4. `Boolean.toString(boolean obj)` --> converts a Boolean to String

[^1]: The inputs required by the method.\


    &#x20;           &#x20;
