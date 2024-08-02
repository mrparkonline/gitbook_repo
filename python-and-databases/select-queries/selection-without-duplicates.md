# Selection without Duplicates

## This Tutorial's Database: `petstore.db`

There are 30 records in a single table called `purchases`

**Fields:**

* `pet_name` -> TEXT column of pet names of customers
* `item_bought` -> TEXT details the type of item bought
* `quantity` -> INTEGER number of the item bought within the purchase session

### Displaying our distinct names of our pet customers

**Query**

```sql
SELECT DISTINCT pet_name 
FROM purchases 
```

```python
# Python w/ SQLite
import sqlite3
connection = sqlite3.connect("petstore.db")
cursor = connection.cursor()

query = '''
SELECT DISTINCT pet_name 
FROM purchases
'''

result = cursor.execute(query)
print(f"Our pet customers: {result.fetchall()}")

cursor.close()
connection.close()
```

**Output**

```
Our pet customers: [
    ('Rocky',), ('Cooper',), ('Bear',), ('Buddy',), ('Bella',), 
    ('Maggie',), ('Zeus',), ('Roxy',), ('Duke',), ('Sophie',), 
    ('Bailey',), ('Chloe',), ('Daisy',), ('Luna',), ('Milo',), 
    ('Charlie',), ('Sadie',)
]
```
