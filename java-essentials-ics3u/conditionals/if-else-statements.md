# If Else Statements

```java
import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

        System.out.println('Enter the day: ')
        String day = in.nextLine();
        
        if (day.equals("Saturday") || day.equals("Sunday")) {
            System.out.println("No school today!");
        }
        else {
            System.out.println("lol, you have school today.");  
        }
    }
}
```

### Making Binary Pathways

By using an `else` statement, we can handle for situation when an `if` statement's boolean expression is `false`.

This allows us to react to a condition being `false`, and it will allow our program to be more complex.

### Common Mistakes

```
// BAD CODE BELOW
if (__CONDITIONA__) {
    // code A
}
if (__CONDITIONB__) {
    // code B
}
else {
    // code C
}
```

> the `else` statement is only related to `__CONDITIONB__`

```
// BAD CODE BELOW
else {
    // code C
}

if (__CONDITIONA__) {
    // code A 
}
```

> you cannot have a random `else` statement without it being attached to an if statement prior to it
