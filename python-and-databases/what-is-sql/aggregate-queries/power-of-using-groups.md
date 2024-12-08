# Power of using Groups

The `GROUP BY` clause in SQL is used to arrange identical data into groups.&#x20;

This is particularly useful when you want to perform aggregate calculations on subsets of data.

**COUNT()**: Counts the number of rows in each group.

```sql
SELECT department, COUNT(*) AS employee_count
FROM employees
GROUP BY department;
```

This query counts the number of employees in each department.

**SUM()**: Calculates the total sum of a numeric column for each group.

```sql
SELECT department, SUM(salary) AS total_salary
FROM employees
GROUP BY department;
```

This query sums up the salaries of employees in each department.

**AVG()**: Computes the average value of a numeric column for each group.

```sql
SELECT department, AVG(salary) AS average_salary
FROM employees
GROUP BY department;
```

This query calculates the average salary in each department.

**MIN()**: Finds the minimum value in a numeric column for each group.

```sql
SELECT department, MIN(salary) AS lowest_salary
FROM employees
GROUP BY department;
```

This query finds the lowest salary in each department.

**MAX()**: Finds the maximum value in a numeric column for each group.

```sql
SELECT department, MAX(salary) AS highest_salary
FROM employees
GROUP BY department;
```

This query finds the highest salary in each department.

The `GROUP BY` clause is essential for summarizing data and generating reports. It helps in analyzing data by grouping rows that have the same values in specified columns and then applying aggregate functions to each group
