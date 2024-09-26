# Exercise Set 4

Comprehension Questions

## Programming Questions

### 1. Factor Counting Program

Create a program that counts the number of factors of the given input.&#x20;

### 2. String Cleaning Program

Write a function that removes non-alphabetical characters from the given string and returns it as a lowercase version of the cleaned string.

{% hint style="info" %}
`cleaner("H E L L 0O!") -> "hello"`

Function:

* 1 argument string

Returns:

* 1 string object
{% endhint %}

### 3. Palindrome Program

Write a function that returns True if the given string argument is a [palindrome](https://www.google.com/search?q=define%3A+palindrome\&oq=define%3A+palindrome\&gs\_lcrp=EgZjaHJvbWUyBggAEEUYOTIGCAEQRRg60gEIMjA1MWowajeoAgCwAgA\&sourceid=chrome\&ie=UTF-8\&safe=active\&ssui=on). Assume that the argument will only contain alphabetical characters.

Example → `'tacocat'` is a palindrome. `'tacodog'` is not a palindrome

### 4. String Consonant Counter

Write a function that counts the number of consonants in the given string argument. Assume that for simplicity, “aeiou” are the only set of vowels in English. The function should return an integer

Example → `"blueberry"` → 6 consonants (including y)

### 5. String Pattern Creator

Write a function that takes an N integer greater than 0 and outputs/prints the following pattern.

| <p>N = 1</p><p><br></p><p>1</p> | <p>N = 2</p><p><br></p><p>1</p><p>10</p> | <p>N = 3</p><p><br></p><p>1</p><p>10</p><p>101</p> | <p>N = 4</p><p><br></p><p>1</p><p>10</p><p>101</p><p>1010</p> | <p>N = 5</p><p><br></p><p>1</p><p>10</p><p>101</p><p>1010</p><p>10101</p> |
| ------------------------------- | ---------------------------------------- | -------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------------------- |

### 6. Anagram Checker

Create a function that checks if the two strings arguments are anagrams. The function should return True if the two strings are anagrams.

**Example:**

| <p><code>bored</code></p><p><code>robed</code></p><p></p><p><code>anagrams</code></p> | <p><code>elbow</code></p><p><code>below</code><br></p><p><code>anagrams</code></p> | <p><code>jake</code></p><p><code>jasper</code></p><p></p><p><code>Not anagrams</code></p> |
| ------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |

### 7. Duplicates between Two Strings

Create a function that takes two string inputs, return a single sorted list of characters that are found in each string.

**Example:**

| <p><code>hello</code></p><p><code>goodbye</code></p><p></p><p><code>[‘e’, ‘o’]</code></p> | <p><code>jake</code></p><p><code>jasper</code></p><p></p><p><code>[‘a’, ‘e’, ‘j’]</code></p> |
| ----------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |

### 8. Mean & Median

Create a function for each statistical analysis tool: mean, and median. Each function should take a single list of integers as an argument, and then output the result.

### 9. Comma Separated Value to a List

Create a function that takes a string argument with a comma separating different integer values. Convert the argument to a list of integers.

Example: `"1,2,3,4,5" → [1,2,3,4,5]`

### 10. List of Random Integers

Create a function that takes 3 arguments: (start, end, frequency). The function should return a list of random \[frequency] many integers from \[start, end].
