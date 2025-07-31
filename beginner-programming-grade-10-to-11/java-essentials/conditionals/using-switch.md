# Using Switch

In Java, a `switch` statement is a control flow construct used for making decisions based on the value of a variable or expression.&#x20;

It allows you to specify multiple possible execution paths based on the value of the expression.&#x20;

The `switch` statement is often used as an alternative to a series of `if-else if-else` statements **when you have a single variable to test against multiple values**.

{% hint style="info" %}
It's important to note that `switch` cases in Java only work with certain data types like `int`, `char`, `byte`, `short`, and `enum`, as well as their corresponding wrapper classes (e.g., `Integer`, `Character`, etc.)
{% endhint %}

## Switch Syntax

```java
switch (expression) {
    case value1:
        // Code to execute if expression matches value1
        break;
    case value2:
        // Code to execute if expression matches value2
        break;
    // More cases as needed
    default:
        // Code to execute if none of the cases match
}
```

### Example:

{% tabs %}
{% tab title="Code" %}
```java
int dayOfWeek = 3;

switch (dayOfWeek) {
    case 1:
        System.out.println("Monday");
        break;
    case 2:
        System.out.println("Tuesday");
        break;
    case 3:
        System.out.println("Wednesday");
        break;
    case 4:
        System.out.println("Thursday");
        break;
    case 5:
        System.out.println("Friday");
        break;
    case 6:
        System.out.println("Saturday");
        break;
    case 7:
        System.out.println("Sunday");
        break;
    default:
        System.out.println("Invalid day");
}
```
{% endtab %}

{% tab title="Explanation" %}
In this example, the `switch` statement is used to print the day of the week based on the value of the `dayOfWeek` variable.&#x20;

The `break` statement is used to exit the `switch` block after each case is executed.&#x20;

If none of the cases match, the code in the `default` block is executed.&#x20;
{% endtab %}
{% endtabs %}

#### Aside: Java 12 Switch Cases

Starting from Java 12, `switch` expressions allow you to use a wider range of data types.

Here's a quick example using `switch` expressions introduced in Java 12:

```java
String fruit = "apple";

String result = switch (fruit) {
    case "apple" -> "It's an apple.";
    case "banana" -> "It's a banana.";
    case "cherry" -> "It's a cherry.";
    default -> "Unknown fruit.";
};

System.out.println(result);
```

In this case, the `switch` expression assigns a value to the `result` variable based on the value of the `fruit` variable. This feature simplifies `switch` usage and allows you to assign values directly to variables.
