# Selection with Limited Number of Outputs

## This Tutorial's Database: `petstore.db`

There are 30 records in a single table called `purchases`

**Fields:**

* `pet_name` -> TEXT column of pet names of customers
* `item_bought` -> TEXT details the type of item bought
* `quantity` -> INTEGER number of the item bought within the purchase session

**Query**

```sql
SELECT * 
FROM purchases
WHERE pet_name = "Bella"
```

The following would select all the purchases by the pet named `"Bella"`.

**Output**

```
# Python Output
[('Bella', 'Food', 7), ('Bella', 'Treats', 1), ('Bella', 'Food', 1)]
```

If we wanted to just grab the very first item in this scenario, we can limit our output by using a `LIMIT` statement

**New Query to Limit our output to only have one**

```sql
SELECT * 
FROM purchases
WHERE pet_name = "Bella"
LIMIT 1
```

**Output**

```
# Python Output
[('Bella', 'Food', 7)]
```

If we wanted to then grab the value after the first one, we can set an `OFFSET`.

**New Query to Offset our output**

<pre class="language-sql"><code class="lang-sql">SELECT * 
FROM purchases
WHERE pet_name = "Bella"
<strong>LIMIT 1 OFFSET 1
</strong></code></pre>

**Output**

```
# Python Output
[('Bella', 'Treats', 1)]
```

### Grabbing the 3rd, 4th, 5th purchases from our table

**Query**

```sql
SELECT * 
FROM purchases
LIMIT 3 OFFSET 3
```

**Python Code**

```python
# Python w/ SQLite
import sqlite3
connection = sqlite3.connect("petstore.db")
cursor = connection.cursor()

query = '''
SELECT * 
FROM purchases
LIMIT 3 OFFSET 3
'''

result = cursor.execute(query)
print(f"Result: {result.fetchall()}")

cursor.close()
connection.close()
```

**Output**

```
Result: [('Buddy', 'Treats', 8), ('Bella', 'Food', 7), ('Maggie', 'Treats', 8)]
```

Exercise

Connected Readings
