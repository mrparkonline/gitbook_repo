# Exercise Set 4

Comprehension Questions

## Programming Questions

### 1. Factor Counting Program

{% embed url="https://www.youtube.com/watch?v=qn7ri0slMP8" %}

Create a program that counts the number of factors of the given input.&#x20;

### 2. String Cleaning Program

{% embed url="https://www.youtube.com/watch?v=pxw1EwdvAtQ" %}

Write a function that removes non-alphabetical characters from the given string and returns it as a lowercase version of the cleaned string.

{% hint style="info" %}
`cleaner("H E L L 0O!") -> "hello"`

Function:

* 1 argument string

Returns:

* 1 string object
{% endhint %}

### 3. Palindrome Program

{% embed url="https://www.youtube.com/watch?v=Krk8I5gyYk4" %}

Write a function that returns True if the given string argument is a [palindrome](https://www.google.com/search?q=define%3A+palindrome\&oq=define%3A+palindrome\&gs\_lcrp=EgZjaHJvbWUyBggAEEUYOTIGCAEQRRg60gEIMjA1MWowajeoAgCwAgA\&sourceid=chrome\&ie=UTF-8\&safe=active\&ssui=on). Assume that the argument will only contain alphabetical characters.

Example → `'tacocat'` is a palindrome. `'tacodog'` is not a palindrome

### 4. String Consonant Counter

{% embed url="https://www.youtube.com/watch?v=EFmnJ6gtTwY" %}

Write a function that counts the number of consonants in the given string argument. Assume that for simplicity, “aeiou” are the only set of vowels in English. The function should return an integer

Example → `"blueberry"` → 6 consonants (including y)

### 5. String Pattern Creator

{% embed url="https://www.youtube.com/watch?v=FvoJHNQzIMM" %}

Write a function that takes an N integer greater than 0 and outputs/prints the following pattern.

| <p>N = 1</p><p><br></p><p>1</p> | <p>N = 2</p><p><br></p><p>1</p><p>10</p> | <p>N = 3</p><p><br></p><p>1</p><p>10</p><p>101</p> | <p>N = 4</p><p><br></p><p>1</p><p>10</p><p>101</p><p>1010</p> | <p>N = 5</p><p><br></p><p>1</p><p>10</p><p>101</p><p>1010</p><p>10101</p> |
| ------------------------------- | ---------------------------------------- | -------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------------------- |

### 6. Anagram Checker

{% embed url="https://www.youtube.com/watch?v=d1uOF0a4NU0" %}

Create a function that checks if the two strings arguments are anagrams. The function should return True if the two strings are anagrams.

**Example:**

| <p><code>bored</code></p><p><code>robed</code></p><p></p><p><code>anagrams</code></p> | <p><code>elbow</code></p><p><code>below</code><br></p><p><code>anagrams</code></p> | <p><code>jake</code></p><p><code>jasper</code></p><p></p><p><code>Not anagrams</code></p> |
| ------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |

### 7. Duplicates between Two Strings

{% embed url="https://www.youtube.com/watch?v=QwZNPdt_arw" %}

Create a function that takes two string inputs, return a single sorted list of characters that are found in each string.

**Example:**

| <p><code>hello</code></p><p><code>goodbye</code></p><p></p><p><code>[‘e’, ‘o’]</code></p> | <p><code>jake</code></p><p><code>jasper</code></p><p></p><p><code>[‘a’, ‘e’, ‘j’]</code></p> |
| ----------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |

### 8. Mean & Median

{% embed url="https://www.youtube.com/watch?v=yHyBGOatwK4" %}

Create a function for each statistical analysis tool: mean, and median. Each function should take a single list of integers as an argument, and then output the result.

### 9. Comma Separated Value to a List & List of Random Integers

{% embed url="https://www.youtube.com/watch?v=rlzi4mcvzA4" %}

Create a function that takes a string argument with a comma separating different integer values. Convert the argument to a list of integers.

Example: `"1,2,3,4,5" → [1,2,3,4,5]`

Create another function that takes 3 arguments: (start, end, frequency).&#x20;

The function should return a list of random \[frequency] many integers from \[start, end].

### 10. Removing Duplicates

{% embed url="https://www.youtube.com/watch?v=Zqc5AZGOjsE" %}

Create a function that removes duplicates from the given list argument.

`Example: [“a”, ”b”, ”c”, “c”, “b”, “c”, “a”, “a”, “d”] → [“a”, “b”, “c”, “d”]`

### 11. Factor List & Prime Checker

{% embed url="https://www.youtube.com/watch?v=VsygfETL9bY" %}

Create a function that returns a list of the integer argument's factor.

Example: `12 returns [1, 2, 3, 4, 6, 12]`

Create a function that returns `True` if the given integer argument is a prime number.

### 12. String Compression

{% embed url="https://www.youtube.com/watch?v=xZphrpezYwY" %}

Implement a function that performs basic string compression using the counts of repeated characters. Return the string if the compression is longer or the same length as the argument.

For example, `"aabcccccaaa"` would become `"a2b1c5a3"`
