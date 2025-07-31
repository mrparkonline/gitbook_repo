# Making Multiple Decisions

```java
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        System.out.println('Enter your age: ')
        int age = in.nextInt();
        
        if (age > 17) {
            System.out.println("You can watch any movies.");
        } else if (age >= 13) {
            System.out.println("You can watch any rated movies except: ");
            System.out.println("You cannot watch NC-17.");
            System.out.println("You require parent/adult guaradian supervision to watch R rated movies.");
            
        } else {
            System.out.println("You can watch G rated movies and you also need parental guidance for PG and PG-13 rated movies.");  
        }
    }
}
```

### Multiple Related Decisions

If you examine the code above, the second conditional statement uses both keywords of `else if`. This is only possible because:

* We have a trailing if statement on the same indentation level
* We are writing a code that relies on checking multiple conditions
* The conditions that we are checking are all related to each other

In the code above, the `else if`'s and `else`'s codes within its blocks will be ignored if the first condition evaluates to True. This occurs when `age` is greater than or equal to 13.

The significant learning point is that the program will not check the next conditions if the first one was true. It will only try to check to other conditions if the prior conditions are false.

### Multiple, but Unrelated Decisions

```java
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        System.out.println("Is it raining? (Yes/No)");
        String weather = in.nextLine();

        System.out.println("Enter a number");
        int num = in.nextInt();

        // Conditions
        if (weather.equals("Yes")) {
            System.out.println("It is raining outside.");
        }
        if (num == 42) {
            System.out.println("You have entered a special number.");
        } else {
            System.out.println("It is just a number.");
        }
        }
    }
}
```

#### Code Explanation

```java
if (weather.equals("Yes")) {
    System.out.println("It is raining outside.");
}
if (num == 42) {
    System.out.println("You have entered a special number.");
}
```

> The two if statements above are not related. Both conditions will evaluated no matter the result of the boolean expressions.

```java
if (weather.equals("Yes")) {
    System.out.println("It is raining outside.");
}
if (num == 42) {
    System.out.println("You have entered a special number.");
} else {
    System.out.println("It is just a number.");
}
```

> The bottom most else statement is only related to our second if statement. The program will not skip to the else statement if the `weather.equals("Yes")` evaluates to false.
>
> The program will output: `It is just a number.` if the variable `num` was not 42.

## Nested Conditionals

```java
if (num > 0) {
    System.out.println("The number is positive.");
            
    if (num % 2 == 0) {
        System.out.println("And it's even.");
    } else {
        System.out.println("And it's odd.");
    }
} else if (num < 0) {
    System.out.println("The number is negative.");
} else {
    System.out.println("The number is zero.");
}
```

**Nested conditional statements** in Java are simply conditional statements within another conditional statement.

_Let's assume that variable `num` has a value `45`._

* We first check if `num` is greater than `0`.&#x20;
  * If it is, we print that the number is positive, then we check if it's even or odd using another <mark style="color:yellow;">**nested**</mark> `if-else` statement.
* If `num` is not greater than `0`, we move to the `else if` part and check if it's less than `0`. If it is, we print that the number is negative.
* If `num` is neither greater than `0` nor less than `0`, it must be `0`, so we print that the number is zero.
