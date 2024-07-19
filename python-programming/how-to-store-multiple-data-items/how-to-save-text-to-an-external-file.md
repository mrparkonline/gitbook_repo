# How to Save Text to an External File

## Goal

We want to save text data to an external file.

This is when we would want a persistent storage. Persistent storage is when we have our data saved and remembered even if our program is done executing.

### Important Definitions

{% hint style="info" %}
#### Reading

The term `reading` is the ability to obtain data from a file or an input source

#### Writing

The term `writing` is the ability to insert data to a file, and create a new content

#### Append

The term `append` is the ability to add new content to a data file without erasing the content within the file

#### A `.txt` file

A `.txt` file is a computer's simplest way to save written content. It is supported by many operating systems, and it does not worry about any type of formatting or design choices (such as font, colour, and font-sizes).
{% endhint %}

### A Starting Point for our Code

_This example code will track customer's phone models to have a related data of a customer having a customer number, customer's name, and their phone's maker (aka Apple or Google)._

```python
# Database Initialization
customers = {} # Empty Dictionary to Store customer data

# Initialize our database size
customer_count = int(input("How many customers: "))

# Based on the the number of users, we will add related user data to the dictionary
for i in range(customer_count):
    customer_key = f"Customer {i}"

    current_name = input(f"User {i}'s name: ")
    phone_company = input("Input user's Phone Maker: ")

    customers[customer_key] = [current_name, phone_company]

print("Our Database:")
print(customers)
```

#### Example Run _(Added custom spacing below for readability)_

The code creates a dictionary with the following features:

* `Key` -> User's ID (Customer and their Number)
* `Value` -> A simple list of string values with their name and the phone's make

<pre><code>How many customers: 3

User 0's name: Marshall
<strong>Input user's Phone Maker: Apple
</strong>
User 1's name: Jasper
Input user's Phone Maker: Google

User 2's name: Freya
Input user's Phone Maker: Samsung

Our Database:
{
    'Customer 0': ['Marshall', 'Apple'], 
    'Customer 1': ['Jasper', 'Google'], 
    'Customer 2': ['Freya', 'Samsung']
}
</code></pre>

The problem with the current code is that every time this code runs, it will create the dictionary during the program's execution and forget the database after the program stops running.

**The simple/basic solution would be to store the contents of the dictionary into a text file.**

## Adding the feature to save the database

```python
# Database Initialization
customers = {} # Empty Dictionary to Store customer data

# Initialize our database size
customer_count = int(input("How many customers: "))

# Based on the the number of users, we will add related user data to the dictionary
for i in range(customer_count):
    customer_key = f"Customer {i}"

    current_name = input(f"User {i}'s name: ")
    phone_company = input("Input user's Phone Maker: ")

    customers[customer_key] = [current_name, phone_company]

print("Our Database:")
print(customers)

# Creating an external file with our database
# Each line will have the following:
#   Customer Number, Customer Name, Customer's Phone Make
# Example:
#   Customer 0, Marshall, Apple

# Step 1: Use the Python's design pattern for creating a new file

with open("database.txt", "w") as new_file:
    # This created a new file called: database.txt
    # We can interact with it in our code by working with the variable called "new_file"
    # The 2nd argument in open() called "w" means we are writing content into the file
    
    # Step 2: 
    # - loop through the dictionary's key and value
    # - format the content to the our desired way
    # - insert it into the txt file

    for key, value in customers.items():
        customer_name = value[0]
        customer_company = value[1]

        written_data = f"{key}, {customer_name}, {customer_company}\n"
        # \n is a special instruction to say that we are adding a linebreak in our .txt file

        new_file.write(written_data)
    # end of for loop
    print("File creation finished.")
# When this code is finished, it will create a new database.txt at the same location of the python file

```

### Program's Terminal Output + Example Run

```
How many customers: 2
User 0's name: Marshall
Input user's Phone Maker: Samsung
User 1's name: Freya
Input user's Phone Maker: Apple
Our Database:
{'Customer 0': ['Marshall', 'Samsung'], 'Customer 1': ['Freya', 'Apple']}
File creation finished.
```

### Contents of `database.txt`

```
Customer 0, Marshall, Samsung
Customer 1, Freya, Apple

```

### Connected Reading

* File Input / Output ([Link](../../02-programming-in-python/file-i-o/))
* Dictionary ([Link](../../02-programming-in-python/dictionary.md))
* List ([Link](../../02-programming-in-python/tuples-and-lists/))
