# Delayed Output in Java

Due to the code containing a lot of intricate content. The contains two static methods that can be implemented into programs to help delay string outputs.

## Two Methods

### Method 1: `delayedMessage()`

The `delayedMessage()` method will output the given message to the console then apply a delay (measured in milliseconds) afterwords. Therefore, any lines of code that happen directly after will be delayed by a given ms parameter.

### Method 2: `typeIt()`

The `typeIt()` method will simulate a person typing out each individual character in a string. The speed of the typing can be set as the second parameter measured in milliseconds.

```java
import java.util.Scanner;

class Sleep {

    /** 
    * This method prints the given message to the console then executes a delay.
    * 
    * @param message is a String object
    * @param ms is an int value to denote intended delay measured in milliseconds
    * 
    * There is no return value.
    */
    public static void delayedMessage(String message, int ms) {
        if (message.length() > 0) {
            try {
                System.out.println(message);
                Thread.sleep(ms);
            } catch (InterruptedException e) {
                // Handle the exception if needed
                e.printStackTrace();
            }
        }
    }

    /** 
    * This method prints simulates a String message parameter being typed out.
    * 
    * @param message is a String object
    * @param ms is an int value to denote intended delay measured in milliseconds
    * 
    * There is no return value.
    */
    public static void typeIt(String message, int ms) {
        if (message.length() > 0) {
            for (int i=0; i < message.length(); i++) {
                try {
                    if (i < message.length()-1) {
                        System.out.print(message.charAt(i));
                        Thread.sleep(ms);
                    }
                    else {
                        System.out.println(message.charAt(i));
                    }
                } catch (InterruptedException e) {
                    // Handle the exception if needed
                    e.printStackTrace();
                }
            }
        }
    }

    public static void main(String[] arg) {
        Scanner sc = new Scanner(System.in);

        // Example of delayed message by 2 seconds. 2 seconds = 2000 milliseconds
        delayedMessage("Hello", 2000);
        System.out.println("World!");

        // Displaying each character at every 250 ms.
        typeIt("Hello World!", 250);

        sc.close();
    }
}
```
