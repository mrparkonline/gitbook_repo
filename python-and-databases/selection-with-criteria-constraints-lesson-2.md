# Selection with Criteria/Constraints: Lesson 2

## Our Lesson 2 Database: `pokemon.db`

_`Table Name: pkmn`_

<table data-full-width="true"><thead><tr><th width="167">name</th><th>pkmn_type1</th><th>pkmn_type2</th><th>number</th></tr></thead><tbody><tr><td>Bulbasaur</td><td>Grass</td><td>Poison</td><td>1</td></tr><tr><td>Charmander</td><td>Fire</td><td></td><td>4</td></tr><tr><td>Squirtle</td><td>Water</td><td></td><td>7</td></tr></tbody></table>

### Selecting based on specific criteria

```sql
SELECT * FROM pkmn WHERE pkmn_type2 IS NULL
```

Will only select records where a Pokemon does have a second type (`pkmn_type2`).&#x20;

This query generates:

<table data-full-width="true"><thead><tr><th>name</th><th>pkmn_type1</th><th>pkmn_type2</th><th>number</th></tr></thead><tbody><tr><td>Charmander</td><td>Fire</td><td></td><td>4</td></tr><tr><td>Squirtle</td><td>Water</td><td></td><td>7</td></tr></tbody></table>

```sql
SELECT number, name FROM pkmn WHERE pkmn_type1 = "Grass"
```

Whereas this query generates:

<table data-full-width="true"><thead><tr><th>number</th><th>name</th></tr></thead><tbody><tr><td>1</td><td>Bulbasaur</td></tr></tbody></table>

Exercises

Connected Reading
