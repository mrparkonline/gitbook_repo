# Exercise Set 2

## Comprehension Questions



## Programming Questions

### 1. A D\&D Ability Check

{% embed url="https://www.youtube.com/watch?v=ZP4ASKX7rzw" %}

{% hint style="info" %}
An **ability check** in Baldur’s Gate 3 is determined by first the Difficulty Class (DC).&#x20;

The DC is a number representing how hard a task is. When a player wants to do something uncertain, like jumping a gap or sneaking past guards, the Dungeon Master (DM) sets a DC. The player rolls a 20-sided die (D20) and adds modifiers from their character to the roll. If the total meets or beats the DC, the action succeeds. If not, it fails. The D20 introduces randomness, making even skilled characters sometimes fail in challenging situations, adding excitement to the game.
{% endhint %}

The program should take in a single integer value representing the DC then randomly roll a value from 1 to 20 inclusively. Determine if the player was successful at succeeding the ability check.

**Solution Code (**[**Link**](https://raw.githubusercontent.com/mrparkonline/ics4u\_2023F/main/video\_solution/vid07.py)**)**

### 2. Tournament Selection ([CCC 2016 - J1](https://dmoj.ca/problem/ccc16j1/pdf))

{% embed url="https://www.youtube.com/watch?v=QrjHqOz1-J8" %}

Each player in a tournament plays six games. There are no ties. The tournament director places the players in groups based on the results of games as follows:

* if a player wins 5 or 6 games, they are placed in Group 1;
* if a player wins 3 or 4 games, they are placed in Group 2;
* if a player wins 1 or 2 games, they are placed in Group 3;
* if a player does not win any games, they are eliminated from the tournament.

Write a program to determine which group a player is placed in.

**Solution Code (**[**Link**](https://raw.githubusercontent.com/mrparkonline/ics4u\_2023F/main/video\_solution/vid08.py)**)**

### 3. Rock Paper Scissors

{% embed url="https://www.youtube.com/watch?v=Us1kfe2zMNA" %}

Create a program that takes two inputs of Rock, Paper, or Scissors to simulate a 1v1 rock paper scissors game between two people.

**Sample Runs of the Code:**

| <p><code>Sample Input:</code></p><p><code>Rock</code></p><p><code>Rock</code></p>     | <p><code>Sample Output:</code></p><p><code>Tie Game.</code></p>      |
| ------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| <p><code>Sample Input:</code></p><p><code>Rock</code></p><p><code>Paper</code></p>    | <p><code>Sample Output:</code></p><p><code>Player 2 Wins.</code></p> |
| <p><code>Sample Input:</code></p><p><code>Rock</code></p><p><code>Scissors</code></p> | <p><code>Sample Output:</code></p><p><code>Player 1 Wins.</code></p> |

**Solution Code (**[**Link**](https://raw.githubusercontent.com/mrparkonline/ics4u\_2023F/main/video\_solution/vid09.py)**)**

### 4. Telemarketer or Not ([CCC 2018 - J1](https://dmoj.ca/problem/ccc18j1/pdf))

{% embed url="https://www.youtube.com/watch?v=JRy3CWtDFZ8" %}

Write a program to decide if a telephone number is a telemarketer number or not, based on the last four digits. If the number is not a telemarketer number, we should answer the phone, and otherwise, we should ignore it.

**Solution Code (**[**Link**](https://raw.githubusercontent.com/mrparkonline/ics4u\_2023F/main/video\_solution/vid10.py)**)**

### 5. Quadrant Selection ([CCC 2017 - J1](https://dmoj.ca/problem/ccc17j1/pdf))

{% embed url="https://www.youtube.com/watch?v=mPHv1YZXJ9o" %}

Your job is to take a \[cartesian] point and determine the quadrant it is in. You can assume that neither of the two coordinates will be 0.

**Solution Code (**[**Link**](https://raw.githubusercontent.com/mrparkonline/ics4u\_2023F/main/video\_solution/vid11.py)**)**

### 6. Triangle Times ([CCC 2014 - J1](https://dmoj.ca/problem/ccc14j1/pdf))

{% embed url="https://www.youtube.com/watch?v=eyLOqRrYT5k" %}

You have trouble remembering which type of triangle is which. You write a program to help.

Your program reads in three angles (in degrees).

* If all three angles are 60, output Equilateral.
* If the three angles add up to 180 and exactly two of the angles are the same, output Isosceles.
* If the three angles add up to 180 and no two angles are the same, output Scalene.

If the three angles do not add up to 180, output Error.

**Solution Code (**[**Link**](https://raw.githubusercontent.com/mrparkonline/ics4u\_2023F/main/video\_solution/vid12.py)**)**

### 7. Special Day ([CCC 2015 - J1](https://dmoj.ca/problem/ccc15j1/pdf))

{% embed url="https://www.youtube.com/watch?v=lethXE2Qu04" %}

February 18 is a special date for the CCC this year.

Write a program that asks the user for a numerical month and numerical day of the month and then determines whether that date occurs before, after, or on February 18.

* If the date occurs before February 18, output the word Before.
* If the date occurs after February 18, output the word After.
* If the date is February 18, output the word Special.

**Solution Code (**[**Link**](https://raw.githubusercontent.com/mrparkonline/ics4u\_2023F/main/video\_solution/vid13.py)**)**
