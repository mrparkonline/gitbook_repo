# While loops w/ Strings

This will be our final programming concept that we use a while loop. We will be accessing individual characters of a string.

## Recipe

1. Assign a variable to represent the length of the string
2. Create a variable initialized to zero to help us "index" the characters in the string
3. While the index variable is less than the length of the string
   1. Repeatedly access the string at the given index
4. Make sure to increase the index towards length of the string to eventually terminate the loop

### Example

```javascript
let word = prompt("Enter a word: ");

let i = 0; // i is the indexing variable
let size = word.length; 

while (i < size) {
    console.log(`Character at index ${i} from ${word} is: ${word.at(i)}`)
    
    i++;
}
```

### Output if word was assigned to `hello, world!`

```
Enter a word: hello, world!
Character at index 0 from hello, world! is: h
Character at index 1 from hello, world! is: e
Character at index 2 from hello, world! is: l
Character at index 3 from hello, world! is: l
Character at index 4 from hello, world! is: o
Character at index 5 from hello, world! is: ,
Character at index 6 from hello, world! is:  
Character at index 7 from hello, world! is: w
Character at index 8 from hello, world! is: o
Character at index 9 from hello, world! is: r
Character at index 10 from hello, world! is: l
Character at index 11 from hello, world! is: d
Character at index 12 from hello, world! is: !
```

## Explanation

1. **Prompt for Input**: The program asks the user to enter a word and stores this word in a variable called `word`.
2. **Initialize Index Variable**: The program sets up a variable to keep track of the current position (or index) in the word, starting at 0 in a variable called `i`.
3. **Get Length of the Word**: The program calculates the total number of characters in the word by accessing the length property and stores this number in another variable called `size`.
4. **While Loop**: The program enters a loop that will continue to run as long as the current index is less than the total number of characters in the word.
5. **Print Character and Index**: Inside the loop, the program prints the current character from the word along with its position (index).
6. **Increment Index**: After printing the character and its index, the program increases the index by 1 to move to the next character.

#### Side Note:

* In JavaScript, you can index a value at a string by using either the method called `.at()` or using the `[]` notation.

```javascript
let word = "code";

console.log(word[2]); // Outputs d
console.log(word.at(2)); // Outputs d
```
