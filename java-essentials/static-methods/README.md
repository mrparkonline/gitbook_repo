# Static Methods

{% embed url="https://www.youtube.com/watch?v=G3MZg5FgZkg" %}

A method is a block of code that performs a specific task or operation.

```java
// Format
public static return_type methodName(param_datatype parameter_list) {
    // Method body (code to be executed)
    // ...
    return return_value; // Optional, depending on the return type
}
```

### Explanation

1. **Return Type:** This specifies the data type of the value that the method returns. If the method doesn't return anything, you should use `void` as the return type.
2. **Method Name:** This is the name of the method. It should be a meaningful name that describes what the method does. Method names follow Java's naming conventions (e.g., camelCase).
3. **Parameter List:** This is a list of input parameters (arguments) that the method accepts. Parameters are optional, and if a method doesn't take any parameters, you should use empty parentheses `()`.
4. **Method Body:** This is where you write the code that performs the desired functionality of the method.
5. **Return Statement:** If the method has a return type other than `void`, you must use the `return` statement to return a value of that type. If the method doesn't return anything, you can omit the `return` statement or use it without a value (`return;`).

### Example Code

```java
// Using the add() method in main()
class Main {
    public static int add(int num1, int num2) {
        int result = num1 + num2;
        return result;
    }
    
    public static void main(String[] args) {
        System.out.println(add(1,2));
    }
}
```

```
// Output
3
```

### Explanation

* `add()` is a _**static**_ method named `add` with two integer parameters, `num1` and `num2`.
* Inside the method, it calculates the sum of `num1` and `num2` and stores the result in a local variable `result`.
* Finally, it returns the `result` as an integer value.

## `static` keyword

A static method is a method that belongs to the class, not to an instance of the class. Static methods can be called using the class name, without creating an object of the class. They are often used for utility functions, where the behavior of the method does not depend on instance-specific state.

#### Key Points

* At this level of Java Programming, we are creating only a single class. This concept of "class" is part of a larger programming paradigm called "[**object oriented programming**](../../ics4u1-content-2023/04-object-oriented-programming/)". This concept is not covered for ICS3U.
* In our **main class,** we design _**named methods**_ that are standalone containers of code that can solve single problems.
* We must have both the **`public`** and **`static`** label on our custom methods.

## Static Method Creation Philosophy

* **Clean Code:** We want organize a solution to problem or a part of a problem into a single function
* **Algorithms:** Without methods, we cannot express algorithms properly
* **Reusability:** The methods that we create can be imported or copied over to new programs to prevent re-coding same problems that has already been solved
* **Single-Serving:** A method should not be solving multiple problems or have multiple algorithms represented. A method should be designed as a standalone program that is solving one problem
