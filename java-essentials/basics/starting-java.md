# Starting Java

### Our Basic Java Program Boilerplate

```java
// Inside Main.java
class Main {
    public static void main(String[] args) {
        // Your java code goes here.
    }
}
```

#### Boilerplate

> Boilerplate code, also known as **boilerplate**, is the part of code that has to be repeatedly in use with no or a little modification.

#### How To Use Our Boilerplate

1. For every [**replit**](https://replit.com/) program we create, we will be coding inside our `Main.java` file.
2. You can copy the boilerplate to help you start your code.
3. Do not modify any code given in the boilerplate, only code in the section under _"your java code goes here."_
4. After you have programmed, you can `run` your code by clicking the run button at top.

#### Our First Java Program

```java
// Inside Main.java
class Main {
    public static void main(String[] args) {
        // Your java code goes here.
        System.out.println("Hello, World!");
    }
}
```

This program is written in Java to output the message `Hello, World!` into the [console](https://jupyterlab.readthedocs.io/en/stable/user/code\_console.html).

```java
System.out.println("Hello, World!");
```

The code above is a way to output a text message to the program's console.

**Key Points for Programming Java.**

1. _Capitalization Matters:_ `System != system`
2. _Indentations Matter:_ It should be **4 spaces per indentation** and it should be consistent for all indentations in your code.

```java
// GOOD:
public static void main(String[] args) {
    // Your java code goes here.
    System.out.println("Hello, World!");
}
// BAD:
public static void main(String[] args) {
  // Your java code goes here.
system.out.printn("Hello, World!");
}
```

3. Most lines in Java ends with a semicolon `;`.
4. Spelling matters: `println vs. printn`
5. The label after `class` should be the same as the file's name

## Recommended Boilerplate for Beginners

```java
// I am assuming your file is called Main.Java

import java.util.Scanner; // This will allow us to do user inputs

class Main {
    public static void main(String[] args) {
        // Create your scanner object
        Scanner sc = new Scanner(System.in);
        
        // Write your code here.
        
        sc.close(); // Always close your scanner object.
    }
}
```

## What is Java?

Java is a compiled, versatile, high-level, and object-oriented programming language known for its platform independence, robustness, and wide range of applications.&#x20;

Developers write Java code and then compile it into platform-neutral bytecode using a **Java compiler**.&#x20;

This bytecode can be executed on various platforms and devices by the Java Virtual Machine (JVM). Java is renowned for its strong support for multi-threading, extensive library ecosystem, and the "write once, run anywhere" philosophy, making it a popular choice for web development, mobile app development, enterprise software, and more.
