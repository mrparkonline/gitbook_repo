# SELECT Queries: Lesson 1

## Our Lesson 1 Database: `pokemon.db`

_`Table Name: pkmn`_

| name       | pkmn\_type1 | pkmn\_type2 | number |
| ---------- | ----------- | ----------- | ------ |
| Bulbasaur  | Grass       | Poison      | 1      |
| Charmander | Fire        |             | 4      |
| Squirtle   | Water       |             | 7      |

[_Aside: What is a Pokemon?_](https://en.wikipedia.org/wiki/Pok%C3%A9mon)

In the table above, we have an example snapshot of a table that exists within `pokemon.db` file  that is included in the lesson1 folder.

### Database Explained

* **Columns (Fields) contain the following data's information**
  * `name -> TEXT` ; represents the names of the pokemon
  * `pkmn_type1 -> TEXT` ; represents the pokemon's type from the game's type structure
  * `pkmn_type2 -> TEXT`; represents the pokemon's second type if applicable
  * `number -> INTEGER`; represents the number  assigned to each pokemon based on the Pokedex order
* **Rows (Records) contain the actual data**
  * Each row within a table will have all, some or none of the column data available for the given data
  * When inserted, the data must follow the datatype rule set by the column

## `SELECT` Query

**Structure**

```sql
SELECT column1_name, column2_name, ... column100_name FROM table_name
```

