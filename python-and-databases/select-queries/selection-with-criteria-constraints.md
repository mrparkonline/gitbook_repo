# Selection with Criteria/Constraints

## Our Lesson 2 Database: `swim.db`

_`Table Name: butterfly200; Showing only first 3 athletes`_

<table data-full-width="true"><thead><tr><th width="298">name</th><th>country</th><th>time</th></tr></thead><tbody><tr><td>Lindsey Mcneil</td><td>Norway</td><td>133831</td></tr><tr><td>Giada Middleton</td><td>Georgia</td><td>144370</td></tr><tr><td>Natalie Patrick</td><td>North Macedonia</td><td>147728</td></tr></tbody></table>

There are 30 athletes included athletes with the following characteristics:

* randomly generated name
* randomly chosen country
* randomly generated time measured in milliseconds
  * 2 minutes is 120,000 milliseconds which is very close to [Canada's Sarah McIntosh's Olympic Record time in 2024](https://www.saanichnews.com/sports/canadian-summer-mcintosh-wins-gold-in-200-metre-butterfly-at-paris-olympics-7467374).

### Selecting based on specific criteria

```sql
SELECT column_info
FROM table_name
WHERE condition
    AND/OR more_conditions
```

The code snippet above is a template of how to choose records that include certain columns which fit the custom condition based criteria

**Some Examples of Conditions**

| SQL Operator          | What does it do?                                | SQL                                         |
| --------------------- | ----------------------------------------------- | ------------------------------------------- |
| `=, !=, < <=, >, >=`  | standard numeric comparisons                    | `column_name != 6`                          |
| `BETWEEN x AND y`     | checking for inclusive range                    | `column_name BETWEEN 1.5 AND 10.5`          |
| `NOT BETWEEN x AND y` | check for numbers outside of an inclusive range | `column_name NOT BETWEEN 1 AND 10`          |
| `IN (x, y, z)`        | value exists in a list                          | `column_name IN ("RED", "GREEN" , "BLUE" )` |
| `NOT IN (x, y, z)`    | value does not exist in a list                  | `column_name NOT IN (3, 1, 4)`              |

```plsql
SELECT name
FROM butterfly200
WHERE time < 130000
```

```python
# Python w/ SQLite
import sqlite3
connection = sqlite3.connect("swim.db")
cursor = connection.cursor()
query = '''
    SELECT name
    FROM butterfly200
    WHERE time < 130000
'''
result = cursor.execute(query)
print("Athletes that finished under 2.16 minutes:")
print(result.fetchall())

cursor.close()
connection.close()
```

This query generates:

```
Athletes that finished under 2.16 minutes:
[('Joslyn Rosario',), ('Saniya Palmer',), ('Jazmin Dixon',), ('Jazlyn Hensley',), ('Haven Dixon',), ('Kamryn Kane',), ('Sierra Mejia',), ('Yasmine Kline',), ('Nia Kane',)]
```

### Finding Spanish, French or Belgian Athletes

**Query:**

```sql
SELECT *
FROM butterfly200
WHERE country IN ("Spain", "France", "Belgium")
```

```python
import sqlite3
connection = sqlite3.connect("swim.db")
cursor = connection.cursor()
query = '''
    SELECT *
    FROM butterfly200
    WHERE 
        country IN ("Spain", "France", "Belgium")
'''
result = cursor.execute(query)
print("Athletes that are from either Spain, France, and Belgium:")
print(result.fetchall())
cursor.close()
connection.close()
```

**Output**

```
Athletes that are from either Spain, France, and Belgium:
[('Chana Bernard', 'Spain', 143712), ('Jazlyn Hensley', 'Belgium', 128358), ('Erin Malone', 'France', 142178)]
```

## Exercises

* Did any randomized athlete beat Sarah McIntosh's Olympic Record of 2 minutes and 3 seconds (123300 milliseconds)?
* Are there any Canadian athletes, are there American (United States) athletes, are there any from your background/home country?
* Who was the fastest athlete?
