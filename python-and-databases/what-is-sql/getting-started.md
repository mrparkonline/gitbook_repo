# Getting Started

## Get the Lesson Contents Forked

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

If you’re using GitHub, start by forking the repository.&#x20;

This creates a **`copy of the repository`** under your GitHub account.&#x20;

You can do this by clicking the “Fork” button at the top right of the repository page.

## Clone Lesson Contents to your Machine

```git
git clone https://github.com/mrparkonline/ib_databases.git
```

This will allow us to clone all the lesson materials required for this chapter into your folder of your choice.&#x20;

This command should be executed in your terminal after you have [**git**](https://git-scm.com/) installed.

## Python + SQLite Model

```
Directory Layout

/lesson#/
      | -- lesson#.py
      | -- database.db
```

`lesson#.py`

The name of the file can be called anything as long as it has `.py` extension as we will be writing both of our Python script and SQL queries via SQLite3 within this file

`database.db`

This file will contain our database that we will be interacting with. Depending on the lessons, the `database.db` may have a different filename and/or contents

### Working Example

`lesson1.py`

```python
# Python + SQLite Lesson 1

# Step 1: import SQLite3 Module
import sqlite3

# Step 2: create a connection with a SQL database file
connection = sqlite3.connect("pokemon.db")

# Step 3: create a cursor that helps us to communicate with a the database
cursor = connection.cursor()

# Step 4: execute SQL queries with a method called ".execute()" from the cursor

# QUERIES GO HERE


# Step 5: Commit your changes on the database
connection.commit()

# Step 6: Optional, see the total number of changes
print(f"Current session's number of changes: {connection.total_changes}")

# Step 7: When finished with the database, close your cursor and connection object
cursor.close()
connection.close()
```

Within lesson 1, we will be exploring a very simple database called `pokemon.db` that exists within the same directory as the Python file.

For Python to interact with a SQL database using SQLite3, we must do the following operations:

1. Import sqlite3 _(a built-in module within Python)_

```python
# Importint the SQLite3 Module
import sqlite3
```

2. Create a connection to a database

```python
# Creating a connection to a database
connection = sqlite3.connect("pokemon.db")

# the connection variable could have been named something else
# the database connected can also be any other database you would like
```

3. Create a cursor to interact with the connected database

```python
# Creating a cursor object 
# the cursur helps us to communicate with a the database
cursor = connection.cursor()

# Main Purpose:
#     1. Execute Queries
#     2. Fetch Results
```

4. Commit changes from the connection

```python
# Commit your changes on the database
connection.commit()

# This is only required when you make changes to a database
# Should be executed when
#     1. You have finished your changes
#     2. Your script is over and you want to end the program after 
#        After you have made your changes
```

5. Close the cursor & connection when finished

```python
# Closing your cursor and connection objects
cursor.close()
connection.close()

# By closing both cursor and connection, 
# we are saying that this python script is not working on the database at the moment
```

Closing the cursor and connection is important because:

* it uses up system resources to read/write/append a database -> by closing, we free up such resources
* it opens up a connection spot -> there are limited number of concurrent connections possible; therefore, releasing a connection means that a new connection can be made

## Connected Readings:

* **SQLite3 Documentation from Python (**[**Link**](https://docs.python.org/3/library/sqlite3.html)**)**
