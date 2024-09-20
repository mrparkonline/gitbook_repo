# Basic Password Generator

{% embed url="https://www.youtube.com/watch?v=vZc9Xdhxz6Q" %}

## Goal

Create a Python script that will generate a password with given parameters.

## Program Requirements

1. Requires password length
2. Requires password criteria
   * _Does it contain uppercase characters?_
   * _Does it include numbers?_
   * _Does it include special characters?_
3. Generate a password with the given constraints
4. Output the generated password

_We are ignoring input validations for this exercise._

## Python Translation

```python
# Basic Password Generator

# module import
import random

# ASCII Table Decimal to Characters
lowercase = list(range(97, 123))
uppercase = list(range(65, 91))
digits = list(range(48, 58))
special = list(range(33, 48)) + list(range(58,65)) + list(range(91,97)) + list(range(123,127))

# initialize empty password
password = "" # Empty String
options = lowercase.copy() # We assume that our passwords will always have at least lowercase characters

# input
# Requirement 1: Set Password Length
size = int(input("Enter the size of the password: "))

# Requirement 2: Set Password Criteria
has_upper = input("Include uppercase letters? (Y/N): ")
has_digit = input("Include numbers? (Y/N): ")
has_special = input("Include special characters? (Y/N): ")

# processing
# Step 1: Add in the respective options
if has_upper in {'Y', 'y'}:
    options.extend(uppercase)

if has_digit in {'Y', 'y'}:
    options.extend(digits)

if has_special in {'Y', 'y'}:
    options.extend(special)

# Step 2:
# Until the password variable meets the desired length, randomly add in
# characters from the our list of options
while len(password) < size:
    random_char = chr(random.choice(options))
    password += random_char

# Requirement 3: Output the generated password
print(f"The randomly generated password is: {password}")
```

### Code Explanation

* **Imports**: The `random` module is imported to generate random characters and numbers.
* **Character Sets**:
  * `lowercase`: Contains ASCII values for lowercase letters (97-122).
  * `uppercase`: Contains ASCII values for uppercase letters (65-90).
  * `digits`: Contains ASCII values for digits (48-57).
  * `special`: Contains ASCII values for special characters (33-47, 58-64, 91-96, 123-126).

{% hint style="info" %}
[What is ASCII?](https://en.wikipedia.org/wiki/ASCII#Printable\_characters)

ASCII stands for American Standard Code for Information Interchange.

ASCII is a character encoding standard that assigns numeric codes to represent characters. Each character, like letters ('A' to 'Z', 'a' to 'z'), digits ('0' to '9'), and special symbols, has a unique integer value in the [**ASCII table**](https://www.cs.cmu.edu/\~pattis/15-1XX/common/handouts/ascii.html).&#x20;

By using the `chr()` function in Python, you can convert these integer values to their corresponding characters, allowing for text representation in digital communications and computing.
{% endhint %}

* **Initialization**:
  * `password`: Starts as an empty string where the generated password will be stored.
  * `options`: Initially set to `lowercase.copy()`, assuming every password will include lowercase letters.
* **User Input**:
  * `size`: User defines the length of the password.
  * `has_upper`, `has_digit`, `has_special`: Users choose whether to include uppercase letters, digits, and special characters, respectively.
* **Processing**:
  * **Step 1**: Based on user input (`has_upper`, `has_digit`, `has_special`), appropriate character sets (`uppercase`, `digits`, `special`) are added to `options`.
  * **Step 2**: A `while` loop continues until `password` reaches the desired length (`size`). In each iteration:
    * `random.choice(options)` picks a random ASCII value from `options`.
    * `chr()` converts the ASCII value to its corresponding character.
    * The character is appended to `password`.
* **Output**:
  * Finally, the generated password (`password`) is displayed to the user.

```
# Example Input
Enter the size of the password: 8
Include uppercase letters? (Y/N): Y
Include numbers? (Y/N): Y
Include special characters? (Y/N): N

# Example Output
The randomly generated password is: qK5g8sHj
```

### Connected Readings

* **Membership Operation (**[**Link**](../../02-programming-in-python/conditionals/comparison-logical-and-membership-operators.md)**)**
* **Strings (**[**Link**](../../02-programming-in-python/strings/)**)**
* **List (**[**Link**](../../02-programming-in-python/tuples-and-lists/)**)**

### General Password Tips

#### Weak Passwords

A weak password is one that is easy to guess or crack, often due to its simplicity, common usage, or predictability. Characteristics of weak passwords include:

* **Short length**: Typically less than 8 characters.
* **Common words or sequences**: Such as "password", "123456", "qwerty", or "abc123".
* **Personal information**: Easily obtainable information like a user’s name, birthdate, or phone number.
* **Lack of variety**: Using only letters, or only numbers, without mixing in other character types.

#### Strong Passwords

A strong password is designed to be difficult to guess or crack, thereby enhancing security. Characteristics of strong passwords include:

* **Long length**: Typically 12 characters or more.
* **Complexity**: A mix of uppercase and lowercase letters, numbers, and special characters (examples: `@, #, $, %`).
* **Unpredictability**: Avoiding common words, phrases, and predictable patterns.
* **Uniqueness**: Different passwords for different accounts to prevent a breach on one site from compromising others.
