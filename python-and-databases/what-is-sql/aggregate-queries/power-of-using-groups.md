# Power of using Groups

The `GROUP BY` clause in SQL is used to arrange identical data into groups.&#x20;

This is particularly useful when you want to perform aggregate calculations on subsets of data.

The `GROUP BY` clause is essential for summarizing data and generating reports.&#x20;

It helps in analyzing data by grouping rows that have the same values in specified columns and then applying aggregate functions to each group

## Our Example Table

`Employees(employeeID, employeeName, salary, department)`

| employeeID | employeeName | salary | department |
| ---------- | ------------ | ------ | ---------- |
| 1          | Alice        | 60000  | HR         |
| 2          | Bob          | 70000  | IT         |
| 3          | Carol        | 65000  | HR         |
| 4          | Dave         | 75000  | IT         |
| 5          | Eve          | 72000  | Sales      |
| 6          | Frank        | 68000  | Sales      |
| 7          | Grace        | 71000  | IT         |
| 8          | Hank         | 69000  | HR         |

### Using `GROUP BY` to obtain information from the `Employee` table

#### Department Sizes

```sql
SELECT department, COUNT(*) AS employee_count
FROM Employees
GROUP BY department;
```

_This query counts the number of employees in each department._

* `employee_count` is an alias(label) that will describe the column that will hold our desired data
* The query above will count how many departments there are by grouping the unique departments then counting how many times it appears in the table

| department | employee\_count |
| ---------- | --------------- |
| HR         | 3               |
| IT         | 3               |
| Sales      | 2               |

#### Total Salary of Departments

```sql
SELECT department, SUM(salary) AS total_salary
FROM Employees
GROUP BY department;
```

_This query sums up the salaries of employees in each department._

* We still group based on the departments
* The new column: `total_salary` will sum up each department member's salary to display

| Department | Total Salary |
| ---------- | ------------ |
| HR         | 194000.0     |
| IT         | 216000.0     |
| Sales      | 140000.0     |

#### Average Salary of Departments

```sql
SELECT department, AVG(salary) AS average_salary
FROM Employees
GROUP BY department;
```

_This query calculates the average salary in each department._

* The new column: `average_salary` will display the average salary of each department

| Department | Average Salary |
| ---------- | -------------- |
| HR         | 64666.67       |
| IT         | 72000.00       |
| Sales      | 70000.00       |

#### **Minimum and Maximum Salaries of Each Department**

```sql
SELECT department, MIN(salary), MAX(salary)
FROM Employees
GROUP BY department;
```

This query finds the lowest salary and highest in each department.

| Department | Min Salary | Max Salary |
| ---------- | ---------- | ---------- |
| HR         | 60000.00   | 69000.00   |
| IT         | 70000.00   | 75000.00   |
| Sales      | 68000.00   | 72000.00   |
