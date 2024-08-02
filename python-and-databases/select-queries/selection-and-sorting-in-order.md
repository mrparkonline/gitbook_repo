# Selection and Sorting in Order

## This Tutorial's Database: `spicy.db`

_`Table Name: hotpeppers; Showing only first 3 peppers`_

| name     | maxSHU | inventory |
| -------- | ------ | --------- |
| Jalapeno | 8000   | 12        |
| Serrano  | 5000   | 7         |
| Habanero | 350000 | 8         |

There are 23 named hot peppers in the dataset

* `name` -> TEXT column of hot pepper names
* `maxSHU` -> INTEGER column of each pepper's maximum level of [Scoville Heat Unit](https://en.wikipedia.org/wiki/Scoville\_scale) range
* `inventory` -> INTEGER column of random counts of how many peppers are available

### Sorting by Inventory from most to least number of items

**Query**

```sql
SELECT * 
FROM hotpeppers 
ORDER BY inventory DESC
```

```python
# Python w/ SQLite
import sqlite3
connection = sqlite3.connect("spicy.db")
cursor = connection.cursor()

query = '''
SELECT * 
FROM hotpeppers 
ORDER BY inventory DESC
'''

result = cursor.execute(query)
print(f"Our wanted pepper data: {result.fetchall()}")

cursor.close()
connection.close()
```

**Output**

```
Our wanted pepper data: [('Fresno', 10000, 19), ('Thai Chili', 100000, 18), ('Chipotle', 8000, 18), ('Piri Piri', 175000, 18), ('Anaheim', 2500, 15), ('Ancho', 2000, 15), ('Carolina Reaper', 2200000, 14), ('Scotch Bonnet', 350000, 14), ('Mulato', 4000, 14), ('Jalapeno', 8000, 12), ('Tepin', 100000, 12), ('Pasilla', 2500, 11), 
('Pepperoncini', 500, 10), ('Hungarian Wax', 15000, 10), ('Habanero', 350000, 8), ("Bird's Eye", 100000, 8), ('Serrano', 5000, 7), ('Ghost Pepper', 1041427, 7), ('Cayenne', 50000, 5), ('Poblano', 2000, 5), ('Chiltepin', 100000, 4), ('Banana Pepper', 500, 2), ('Hatch Chile', 2500, 1)]
```

We can add an `ORDER BY` statement to sort based on column. We can also add `ASC` for least to greatest or `DESC` for the opposite.

An `ORDER BY` statement should be written after a `WHERE` clause

## Exercise

* List the names of peppers in alphabetical order with a query
* List all the pepper data ordered from least to most spicy
