# Arithmetic

### Math Operators in Java

| Symbols       | Operator       | Description                            |
| ------------- | -------------- | -------------------------------------- |
| +             | Addition       | Adds together two values               |
| -             | Subtraction    | Subtracts one value from another       |
| \*            | Multiplication | Multiplies two values                  |
| /             | Division       | Divides one value by another           |
| %             | Modulus        | Returns the division remainder         |
| ++            | Increment      | Increases the value of a variable by 1 |
| --            | Decrement      | Decreases the value of a variable by 1 |
| Math.pow(a,b) | Exponentiation | Calculates the result of $$a^b$$       |

### Code Examples

```java
class Main {
    public static void main(String[] args) {
        int x = 10;
        int y = 5;
        int z = 1;

        int a = x + y;
        System.out.println("Result: " + a); // Expecting 15

        int b = z - y;
        System.out.println("Result: " + b); // Expecting -4

        int c = x * y;
        System.out.println("Result: " + c); // Expecting 50

        int d = x / y;
        System.out.println("Result: " + d); // Expecting 2

        int e = 10 % 3;
        System.out.println("Result: " + e); // Expecting 1 ... remainder of 1
        z++;
        System.out.println("Z: " + z); // Z is now 2

        z--;
        System.out.println("Z: " + z); // Z is now back to 1
        
        System.out.println("Math.pow(2,4): " + Math.pow(2,4)); // Outputs: 16
    }
}
```
