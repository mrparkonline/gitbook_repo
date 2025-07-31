# Basic Built-in Methods

All the methods that are being printed can also have their result set to a variable.

### Anatomy of a Method

`name(arg1, arg2 ...)`

* `name` is where a method name would go
* `()` is where we can place our require arguments for the method
* `arg1` is a placeholder for a possible argument

#### Example: `System.out.println("Hello, World!")`

* `System.out.println` is the name of our method
* `"Hello, World!"` is our argument provided to our method

### Math Methods

```java
double a = 10.3;
double b = 10.5;
double c = 10.6;

System.out.println(Math.round(a)); // Outputs: 10
System.out.println(Math.round(b)); // Outputs: 11
System.out.println(Math.round(c)); // Outputs: 11
```

> `Math.round()` converts your double to the nearest integer value.

```java
double val1 = 4.3;
System.out.println(Math.ceil(4.3)); // Outputs 5.0

double val2 = 4.8;
System.out.println(Math.floor(4.8)); // Outputs 4.0
```

> `Math.ceil()` stands for "ceiling" and rounds a number up to the nearest integer.&#x20;
>
> For example, `Math.ceil(4.3)` would return `5.0`.
>
>
>
> `Math.floor()` stands for "floor" and rounds a number down to the nearest integer. For example, `Math.floor(4.8)` would return `4.0`.
>
> These functions are often used when you need to work with whole numbers or want to adjust a decimal number to the nearest integer in a specific direction

```java
int x = 10;
int y = 5;

System.out.println(Math.min(x,y)); // Outputs: 5
System.out.println(Math.max(x,y)); // Outputs: 10
```

> `Math.min()` will provide the smaller value between the two arguments provided
>
> `Math.max()` will provide the larger value between the two arguments provided

```java
double num =  25.0;
System.out.println(Math.sqrt(num)); // Outputs: 5
```

> `Math.sqrt` will return a square root of the given numeric argument

```java
double fun_value = Math.random();
System.out.println("Random: " + fun_value); // Outputs: Random: 0.1243868832888797
```

> `Math.random()` requires no arguments; it generates a random number from 0 to 1 (not including)
>
> _For my execution of the code it generated 0.1243868832888797_

### Basic String Methods

```java
String text = "Hello, World!";
int text_length = text.length(); // text_length is 13
```

> Since `text` is a string type variable, we can access its methods (_its super powers_) by inserting a period`.` after the variable name.
>
> `.length()` will provide the number of characters that made up the strings

```java
String txt = "Hello World";
System.out.println(txt.toUpperCase());   // Outputs "HELLO WORLD"
System.out.println(txt.toLowerCase());   // Outputs "hello world"
```

> `.toUpperCase()` converts the string to all uppercase
>
> `.toLowerCase()` converts the string to all lowercase
