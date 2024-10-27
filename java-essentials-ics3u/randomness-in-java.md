# Randomness in Java

{% embed url="https://www.youtube.com/watch?v=isdwylC8J5E" %}

In computer programming, true randomness is challenging to achieve because computers are fundamentally deterministic machines. Pseudorandom number generators (PRNGs) are used to simulate randomness by generating sequences of numbers that exhibit statistical properties similar to those of truly random sequences. The key distinction is that PRNGs are deterministic algorithms, meaning that the same initial state (seed) will produce the same sequence of numbers.

## How to Generate Randomness in Java

### Overview

1. Import the Random library class
2. Create a Random object
3. Use the Random object's built-in methods

### Setting up your code

```java
import java.util.Random; // import Random Library/Class

class Main {
    public static void main(String[] arg) {
        Random rand = new Random();
        
        rand.nextBoolean(); // .nextBoolean() generates either True or False at almost equal probability
        rand.nextDouble(); // .nextDouble() generates a random number from 0.0 (inclusive) to 1.0 (exclusive)
        
        int upperBound = 100;
        rand.nextInt(upperBound); // .nextInt(int upperBound) generates a random integer from 0 (inclusive) to upperBound (exclusive)
    }
}
```

### Available Methods

`.nextBoolean()` generates either True or False at almost equal probability

&#x20;`.nextDouble()` generates a random number from 0.0 (inclusive) to 1.0 (exclusive)&#x20;

`.nextInt(int upperBound)` generates a random integer from 0 (inclusive) to upperBound (exclusive)

_More can be found_ [_here_](https://docs.oracle.com/javase/8/docs/api/java/util/Random.html)_._

### Example  1: Heads or Tails.

```java
// Example 1: Heads or Tails?
boolean coin = rand.nextBoolean(); // let heads be true; let tails be false
// using .nextBoolean(); to generate random true or false
        
if (coin) {
    System.out.println("The coin shows head.");
}
else {
    System.out.println("The coin shows tail.");
}

```

This code assigns variable `coin` to contain either `true` or `false` at every run of the program. True will dictate to the coin showing head; False will dictate to the coin showing tail.

### Example 2: Generating Random Decimals

```java
// Example 2: Generating 4 random decimals;
for (int i=0; i<4; i++) {
    double num = rand.nextDouble();
    // using .nextDouble(); to generate random decimal
    System.out.println("Random Decimal: " + num);
}
```

This code is using `rand.nextDouble()` and assigns it to variable `num`. Everytime the random method is executed, it updates the variable with a new number from 0.0 to 1.0 (exclusively).

### Example 3: Choosing a random item from an ArrayList

<pre class="language-java"><code class="lang-java"><strong>ArrayList&#x3C;String> fruits = new ArrayList&#x3C;String>();
</strong>fruits.add("Watermelon");
fruits.add("Grapes");
fruits.add("HoneyDew");
fruits.add("Blueberry");
fruits.add("Strawberry");
fruits.add("Orange");
fruits.add("Banana");
System.out.println("Our fruits: " + fruits);

String rand_fruit = fruits.get(rand.nextInt(fruits.size()));
System.out.println("Random Fruit: " + rand_fruit);
</code></pre>

This code utilizes random integers to help grab a random item from an ArrayList.

* The ArrayList called `fruits` contains 7 items. Therefore, `fruits.size()` returns 7.
* `rand.nextInt()` can only generate an integer from 0 to the given integer parameter. Therefore, it can only generate `0, 1, 2, 3, 4, 5, 6` in this situation given the size of the ArrayList as its parameter.
* `fruits.get(int i)` is an access method that returns an item located at the parameter index of `i.` In this situation, it will grab a fruit at a randomly generated index of: `0, 1, 2, 3, 4, 5, 6`
