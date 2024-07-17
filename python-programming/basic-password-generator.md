# Basic Password Generator

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
has_special = input("Include uppercase letters? (Y/N): ")

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
