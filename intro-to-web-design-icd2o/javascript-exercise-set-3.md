# JavaScript Exercise Set 3

## Simple Problems

1. Create a program that adds all the numbers from 1 up to the user inputted numeric value.
2. Create a program that asks for 10 numbers; average of the inputted numbers.
   1. **Bonus:** let the user decide when to stop inputting the numbers.
3. Create a program that makes the user continuously guess a WORD (string) until they get the secret word set by you the programmer correct.
4. `“FizzBuzz.”` From 1 to 50, if the number is a multiple of three: print `“Fizz”`, if the number is a multiple of five: print `“Buzz”`, if they are multiples of both: print `“FizzBuzz”`.

## Challenging Problems

### Vowel Counter

Assume that our vowels in our alphabet are only from this set: `a e i o u`.

Given a string input from the user, determine and output the number vowels within it.

```
// Sample Input
Hello, World!

// Sample Output
3
```

There are two vowels in `Hello` and one vowel in `World!`.

### Tournament Selection (CCC 2016 J1)

Each player in a tournament plays six games. There are no ties. The tournament director places the players in groups based on the results of games as follows:

* if a player wins 5 or 6 games, output `1` as they are placed in Group 1;
* if a player wins 3 or 4 games, output `2` as they are placed in Group 2;
* if a player wins 1 or 2 games, output `3` as they are placed in Group 3;
* if a player does not win any games, they are eliminated from the tournament; output`-1`

Write a program to determine which group a player is placed in when given 6 inputs of either `W` for a win and `L` for a loss.

```
// Sample Input
W
L
W
W
L
W
// Sample Output
2
```

### Up and Down

Write a program that will count up from 1 to the user's inputted number, and count down back towards 1.

```
// Sample Input
5
// Sample Output
1
2
3
4
5
4
3
2
1
```

### Rock Paper Scissors

Create a two player game of [Rock Paper Scissors](https://en.wikipedia.org/wiki/Rock\_paper\_scissors). There will be two inputs: player 1's choice and player 2's choice.

The game should end after a single player has won 5 times. Output who won.

### Prime Number Checker

Create a program that determines if the user inputted number of 2 or greater is a [prime number](https://en.wikipedia.org/wiki/Prime\_number).

### Palindrome Checker

A palindrome is a word that is the same spelt forwards and backwards.

Some examples of [Palindromes](https://en.wikipedia.org/wiki/Palindrome):

* civic
* madam
* level
* mom
* racecar
* tacocat

Create a program that determines if the inputted word is a palindrome.

### Twenty Questions

Create a program that plays a “20 Questions” game to guess a positive integer between 1 and 100 that the user has in mind.&#x20;

* The user will be instructed by the program to think of a single positive integer from 1 to 100 inclusively
* The program will win if it can guess the number that the user is thinking of in 20 questions or less
* The user will win if the program fails to guess the number
* The user does not need to input their number that they are thinking

The program will ask the user a series of yes/no questions to narrow down the possible numbers and will attempt to guess the number within 20 questions.
