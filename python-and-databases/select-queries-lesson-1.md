# SELECT Queries: Lesson 1

## Python Code Template

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

# Step 5: when finished with the database, close your cursor and connection
cursor.close()
connection.close()
```

## Our Lesson 1 Database: `pokemon.db`

_`Table Name: pkmn`_

<table data-full-width="true"><thead><tr><th>name</th><th>pkmn_type1</th><th>pkmn_type2</th><th>number</th></tr></thead><tbody><tr><td>Bulbasaur</td><td>Grass</td><td>Poison</td><td>1</td></tr><tr><td>Charmander</td><td>Fire</td><td></td><td>4</td></tr><tr><td>Squirtle</td><td>Water</td><td></td><td>7</td></tr></tbody></table>

[_Aside: What is a Pokemon?_](https://en.wikipedia.org/wiki/Pok%C3%A9mon)

In the table above, we have an example snapshot of a table that exists within `pokemon.db` file  that is included in the lesson1 folder.

### Database Explained

* **Columns (Fields, Properties) contain the following data's information**
  * `name -> TEXT` ; represents the names of the pokemon
  * `pkmn_type1 -> TEXT` ; represents the pokemon's type from the game's type structure
  * `pkmn_type2 -> TEXT`; represents the pokemon's second type if applicable
  * `number -> INTEGER`; represents the number  assigned to each pokemon based on the Pokedex order
* **Rows (Records, Instances) contain the actual data**
  * Each row within a table will have all, some or none of the column data available for the given data
  * When inserted, the data must follow the datatype rule set by the column

## `SELECT` Query

**Structure**

```sql
SELECT column1_name, column2_name, ... column100_name FROM table_name
```

To retrieve (see -or- lookup) data from a SQL database, we can use a `SELECT` statement.

In SQL, commands that are reserved for SQL are to be capitalized.

### Get all data from a table

```sql
SELECT * FROM pkmn
```

The following statement will generate:

<table data-full-width="true"><thead><tr><th>name</th><th>pkmn_type1</th><th>pkmn_type2</th><th>number</th></tr></thead><tbody><tr><td>Bulbasaur</td><td>Grass</td><td>Poison</td><td>1</td></tr><tr><td>Charmander</td><td>Fire</td><td></td><td>4</td></tr><tr><td>Squirtle</td><td>Water</td><td></td><td>7</td></tr></tbody></table>

#### Python Code

```python
# Between Step 4 & Step 5.
# 1. Define your query in a multi-line string
query = ''' 
SELECT * FROM pkmn
'''

# 2. Run the query using cursor's execute method
result = cursor.execute(query)

# 3. See all the data provided by .fetchall() method from 
#    the cursor object called result
print(f"Our Query Result:\n{result.fetchall()}")
```

#### Python Output:

```
Our Query Result:
[('Bulbasaur', 'Grass', 'Poison', 1), ('Charmander', 'Fire', None, 4), ('Squirtle', 'Water', None, 7)]
```

### Get data from a single column

```sql
SELECT name FROM pkmn
```

<table data-full-width="true"><thead><tr><th>name</th></tr></thead><tbody><tr><td>Bulbasaur</td></tr><tr><td>Charmander</td></tr><tr><td>Squirtle</td></tr></tbody></table>

You can specify which columns are you are interested by explicitly stating the columns of interest.

#### Python Code

```python
# Between Step 4 & Step 5.
# 1. Define your query in a multi-line string
query = ''' 
SELECT name FROM pkmn
'''

# 2. Run the query using cursor's execute method
result = cursor.execute(query)

# 3. See all the data provided by .fetchall() method from 
#    the cursor object called result
print(f"Our Query Result:\n{result.fetchall()}")
```

#### Python Output:

```
Our Query Result:
[('Bulbasaur',), ('Charmander',), ('Squirtle',)]
```

### Selecting multiple columns

```sql
SELECT number, name FROM pkmn
```

<table data-full-width="true"><thead><tr><th>number</th><th>name</th></tr></thead><tbody><tr><td>1</td><td>Bulbasaur</td></tr><tr><td>4</td><td>Charmander</td></tr><tr><td>7</td><td>Squirtle</td></tr></tbody></table>

```python
# Between Step 4 & Step 5.
# 1. Define your query in a multi-line string
query = ''' 
SELECT number, name FROM pkmn
'''

# 2. Run the query using cursor's execute method
result = cursor.execute(query)

# 3. See all the data provided by .fetchall() method from 
#    the cursor object called result
print(f"Our Query Result:\n{result.fetchall()}")
```

#### Python Output:

```
Our Query Result:
[(1, 'Bulbasaur'), (4, 'Charmander'), (7, 'Squirtle')]
```

As you can see the column order does not matter as long as your choose column names that exists.

### Selecting based on specific criteria

```sql
SELECT * FROM pkmn WHERE pkmn_type2 IS NULL
```

Will only select records where a Pokemon does have a second type. This query generates:

<table data-full-width="true"><thead><tr><th>name</th><th>pkmn_type1</th><th>pkmn_type2</th><th>number</th></tr></thead><tbody><tr><td>Charmander</td><td>Fire</td><td></td><td>4</td></tr><tr><td>Squirtle</td><td>Water</td><td></td><td>7</td></tr></tbody></table>

```sql
SELECT number, name FROM pkmn WHERE pkmn_type1 = "Grass"
```

Whereas this query generates:

<table data-full-width="true"><thead><tr><th>number</th><th>name</th></tr></thead><tbody><tr><td>1</td><td>Bulbasaur</td></tr></tbody></table>

Exercises

Connected Reading
