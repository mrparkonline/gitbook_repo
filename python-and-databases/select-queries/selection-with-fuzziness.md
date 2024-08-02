# Selection with Fuzziness

## Fuzzy Search

A fuzzy search is a technique that uses search algorithms to find strings that match patterns approximately.&#x20;

It's particularly useful when looking for data without knowing exactly what they're looking for or how a word is spelled.

## This Tutorial's Database: `spicy.db`

_`Table Name: hotpeppers; Showing only first 3 athletes`_

| name     | maxSHU | inventory |
| -------- | ------ | --------- |
| Jalapeno | 8000   | 12        |
| Serrano  | 5000   | 7         |
| Habanero | 350000 | 8         |

There are 23 named hot peppers in the dataset

* `name` -> TEXT column of hot pepper names
* `maxSHU` -> INTEGER column of each pepper's maximum level of [Scoville Heat Unit](https://en.wikipedia.org/wiki/Scoville\_scale) range
* `inventory` -> INTEGER column of random counts of how many peppers are available

## Exact Matching and Case-Insensitive Matching

**Query**

```sql
SELECT * 
FROM hotpeppers 
WHERE name = "serrano"
```

```python
# Python w/ SQLite
import sqlite3
connection = sqlite3.connect("swim.db")
cursor = connection.cursor()

query = '''
SELECT * 
FROM hotpeppers 
WHERE name = "serrano"
'''

result = cursor.execute(query)
print(f"Our wanted pepper data: {result.fetchall()}")

cursor.close()
connection.close()
```

**Output**

```
Our wanted pepper data: []
```

Although the 2nd row contains a pepper called `Serrano` since the `S` is capitalized our query could not select the pepper we wanted because the `=` needs an exact match

### `LIKE` operation

We can use the `LIKE` operator to do case-insensitive comparison

**Query**

```sql
SELECT * 
FROM hotpeppers 
WHERE name LIKE "serrano"
```

```python
# Python w/ SQLite
import sqlite3
connection = sqlite3.connect("swim.db")
cursor = connection.cursor()

query = '''
SELECT * 
FROM hotpeppers 
WHERE name LIKE "serrano"
'''

result = cursor.execute(query)
print(f"Our wanted pepper data: {result.fetchall()}")

cursor.close()
connection.close()
```

**Output**

```
Our wanted pepper data: [('Serrano', 5000, 7)]
```

### Finding all pepper names that end in `"no"`

**Query**

```sql
SELECT * 
FROM hotpeppers 
WHERE name LIKE "%no"
```

```python
# Python w/ SQLite
import sqlite3
connection = sqlite3.connect("swim.db")
cursor = connection.cursor()

query = '''
SELECT * 
FROM hotpeppers 
WHERE name LIKE "%no"
'''

result = cursor.execute(query)
print(f"Our wanted pepper data: {result.fetchall()}")

cursor.close()
connection.close()
```

**Output**

```
Our wanted pepper data: [
    ('Jalapeno', 8000, 12), 
    ('Serrano', 5000, 7), 
    ('Poblano', 2000, 5), 
    ('Fresno', 10000, 19)
]

# Output was formatted for readability
```

The `%` wildcard character is used with the `LIKE` operator to perform pattern matching in queries. It represents zero or more characters in a string.

1. **`%` at the Beginning**:
   * Matches any sequence of characters before the specified pattern.
   * Example: `LIKE '%apple'` matches strings ending with "apple" (e.g., "green apple", "red apple").
2. **`%` at the End**:
   * Matches any sequence of characters following the specified pattern.
   * Example: `LIKE 'apple%'` matches strings starting with "apple" (e.g., "apple pie", "apple tart").
3. **`%` in the Middle**:
   * Matches any sequence of characters surrounding the specified pattern.
   * Example: `LIKE '%apple%'` matches strings containing "apple" anywhere (e.g., "green apple pie", "pineapple").
4. **Multiple `%` Wildcards**:
   * You can use multiple `%` wildcards to match complex patterns.
   * Example: `LIKE '%a%ple%'` matches strings that have "a" followed by "ple" somewhere in between (e.g., "apple pie", "pineapple").

### Finding all peppers in the database that are composed of two words

_We are assuming that there will be a whitespace in between each word_

**Query**

```sql
SELECT * 
FROM hotpeppers 
WHERE name LIKE "% %"
```

```python
# Python w/ SQLite
import sqlite3
connection = sqlite3.connect("swim.db")
cursor = connection.cursor()

query = '''
SELECT * 
FROM hotpeppers 
WHERE name LIKE "% %"
'''

result = cursor.execute(query)
print(f"Our wanted pepper data: {result.fetchall()}")

cursor.close()
connection.close()
```

**Output**

```
Our wanted pepper data: [
    ('Thai Chili', 100000, 18), 
    ('Carolina Reaper', 2200000, 14), 
    ('Ghost Pepper', 1041427, 7), 
    ('Banana Pepper', 500, 2), 
    ('Piri Piri', 175000, 18), 
    ('Scotch Bonnet', 350000, 14), 
    ("Bird's Eye", 100000, 8), 
    ('Hatch Chile', 2500, 1), 
    ('Hungarian Wax', 15000, 10)
]

# Output was formatted for readability
```

### Finding pepper data with names that don't have `"Pepper"` as the second word of the name

_This is when the `NOT` operator can be handy_

**Query**

```sql
SELECT * 
FROM hotpeppers 
WHERE name NOT LIKE "%Pepper"
```

```python
# Python w/ SQLite
import sqlite3
connection = sqlite3.connect("swim.db")
cursor = connection.cursor()

query = '''
SELECT * 
FROM hotpeppers 
WHERE name NOT LIKE "%Pepper"
'''

result = cursor.execute(query)
print(f"Our wanted pepper data: {result.fetchall()}")

cursor.close()
connection.close()
```

**Output**

```
Our wanted pepper data: [
    ('Jalapeno', 8000, 12), 
    ('Serrano', 5000, 7), 
    ('Habanero', 350000, 8), 
    ('Cayenne', 50000, 5), 
    ('Thai Chili', 100000, 18), 
    ('Carolina Reaper', 2200000, 14), 
    ('Poblano', 2000, 5), 
    ('Anaheim', 2500, 15), 
    ('Chipotle', 8000, 18), 
    ('Fresno', 10000, 19), 
    ('Piri Piri', 175000, 18), 
    ('Scotch Bonnet', 350000, 14), 
    ('Pepperoncini', 500, 10),
    ("Bird's Eye", 100000, 8), 
    ('Hatch Chile', 2500, 1), 
    ('Tepin', 100000, 12), 
    ('Mulato', 4000, 14), 
    ('Pasilla', 2500, 11), 
    ('Ancho', 2000, 15), 
    ('Hungarian Wax', 15000, 10), 
    ('Chiltepin', 100000, 4)
]

# Output was formatted for readability
```

## Exercises

* Write a query that returns `maxSHU` values of all peppers with names that are not two worded
* Write a query that finds a pepper that has 5 characters only and has the letters `nch` in the middle
* Which pepper is the spiciest and which pepper is not the spiciest?
* Which pepper do we have the most of?

## Connected Reading

* **Fuzzy Search (**[**Wikipedia Link**](https://en.wikipedia.org/wiki/Approximate\_string\_matching)**)**
