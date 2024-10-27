# String Formatting

## What is String Formatting?

We format strings in Java for **clarity, control, and consistency**. It enhances code readability, allows us to precisely present data (numbers, dates, etc.), and ensures consistent output across the application. This improves maintainability, user experience, and sometimes even efficiency.

### String Specifiers

We use specifiers to be a placeholder of where a data should be placed in a String.

| Specifier | Explanation                                                                                                                         |
| --------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| %s        | Converts the data attached automatically to a String equivalent data                                                                |
| %d        | Used for Integers, allows the placement of integers within a string                                                                 |
| %f        | Used for decimals/floats/doubles. This allows decimal values to be represented in a string. You can also control the decimal place. |

### **Formatting a string**

```java
String name = "Alice";
String greeting = String.format("Hello, %s!", name);
System.out.println(greeting); // Output: Hello, Alice!
```

### **Formatting numbers:**

```java
int age = 30;
String message = String.format("My age is %d.", age);
System.out.println(message); // Output: My age is 30.
```

### Formatting numbers with decimals:

```java
double price = 123.456789;
String formattedPrice = String.format("%.2f", price);
System.out.println(formattedPrice); // Output: 123.46
```

### **Using multiple arguments:**

```java
String firstName = "Bob";
String lastName = "Smith";
String fullName = String.format("%s %s", firstName, lastName);
System.out.println(fullName); // Output: Bob Smith
```
