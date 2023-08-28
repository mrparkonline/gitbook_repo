# Boolean Operators

To allow programs to make decisions, we must use the combination of Boolean operators and if statements _(Future Lesson)_.

These operators are binary operators that require a **LEFT OPERAND** and a **RIGHT OPERAND**. The operator will produce a Boolean result of `true` or `false`.

### Comparison Operators

These operators compare the left and the right operand and return `true` if the condition is satisfied.

> let `x` be a variable and `y` be a variable that contains comparable values

| Operation | Description                                                                                       |
| --------- | ------------------------------------------------------------------------------------------------- |
| `x == y`  | Checks if the values of two operands are equal, if YES: returns `true`.                           |
| `x != y`  | Checks if the values of two operands are not equal to each other, if YES: returns `true`.         |
| `x > y`   | Checks if the LEFT operand is greater than the RIGHT operand, if YES: returns `true`.             |
| `x < y`   | Checks if the LEFT operand is less than the RIGHT operand, if YES: returns `true`.                |
| `x >= y`  | Checks if the LEFT operand is greater than OR equal to the RIGHT operand, if YES: returns `true`. |
| `x <= y`  | Checks if the LEFT operand is less than OR equal to the RIGHT operand, if YES: returns `true`.    |

All the operation above return `false` if the condition is not met.

### Logical Operators

Logical Operators are used to combine boolean expressions.

#### Logical AND Operator: `&&`

In Java, multiple boolean expressions can be combined by the `&&` operator.

This operator returns `true` if both sides of the operands evaluate to `true`. Otherwise it will be `false`.

**Example Use of the AND operator:**

> If the train is late to the station **AND** there are no cabs at the station, I am late to work.

```
Their are two boolean conditions:
1. Train is late or not late
2. There are not cabs

The person being late is dependent on BOTH conditions being TRUE. 

The two conditions are combined by a Logical AND operation.
```

#### Logical OR Operator: `||`

In Java, multiple boolean expressions can be combined by the `||` operator.

This operator returns `true` if both sides OR either sides of the operands evaluate to `true`. It only returns `false` if both sides of the operands evaluated to `false`.

**Example Use of the OR operator:**

> I only snack if I am hungry **OR** if I am bored.

```
Their are two boolean conditions:
1. Person is hungry
2. Person is bored

The person being late is dependent on EITHER conditions being TRUE OR BOTH conditions being true.

The two conditions are combined by a Logical OR operation.
```

#### Logical NOT Operator: `!`

In Java, `!` is used to reverse a boolean expression's boolean result.

| Operation  | Result  |
| ---------- | ------- |
| `!(true)`  | `false` |
| `!(false)` | `true`  |

**Example Use of the NOT operator:**

> If it is **NOT** a weekday, I don't go to school

```
The person is dependent on not going to school when it is not a weekday.

On Monday to Friday, the condition of being a weekday is true
    --> Therefore, the "NOT weekday" evaluates to false hench they go to school.

On Saturday & Friday, the condition being a weekday is false
    --> Therefore, the "NOT weekday" evaluates to true hence they don't go to school.
```

### Code Examples on Java

```java
class Main {
    public static void main(String[] args) {
        System.out.println("Boolean Operations in Java.");

        int x = 10;
        int y = 15;

        System.out.println("Is x == y?: " + (x == y));
        System.out.println("Is x != y?: " + (x != y));
        System.out.println("Is x > y?: " + (x > y));
        System.out.println("Is x < y?: " + (x < y));
        System.out.println("Is x >= y?: " + (x >= y));
        System.out.println("Is x <= y?: " + (x <= y));

        int grade = 10;
        int average = 81;

        System.out.println("Are you in grade 10 and have an average higher than or equal to 80?: " + (grade == 10 && average >= 80));

        String fav_fruit = "blueberry";
        System.out.println("Is your favourite fruit blueberry or kiwi?: " + (fav_fruit == "blueberry" || fav_fruit == "kiki"));
        
        boolean weekday = true;
        System.out.println("Do you not go to school today?: " + (!(weekday)));
        
    }
}
```

### SOURCES

* tutorialpoint -- [https://www.tutorialspoint.com/Java-Boolean-operators](https://www.tutorialspoint.com/Java-Boolean-operators)
