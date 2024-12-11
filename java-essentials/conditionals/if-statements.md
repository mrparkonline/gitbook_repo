# If Statements

```java
class Main {
    public static void main(String[] args) {
        String day = "Saturday";

        if (day.equals("Saturday") || day.equals("Sunday")) {
            System.out.println("No school today!");
        }
    }
}
```

One way to _control_ and _make decisions_ in programming is the use of `if statements`.

The code above only executes the message: `No school today!`, if the day is either Saturday or Sunday.

If the day variable was set to something other than Saturday or Sunday, this program would have no output.

### How to Format an If Statement

```
if (__BOOLEAN_CONDITION__) {
    // insert code in here
}
```

> As long as the boolean condition within the parentheses evaluate to `true` the code within the [code block](https://press.rebus.community/programmingfundamentals/chapter/code-blocks/) will execute.
