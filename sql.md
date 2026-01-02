# SQL Cheat Sheet

## 1. The CRUD Operations
CRUD stands for **Create, Read, Update, and Delete**. These are the four basic functions of persistent storage.

| Operation | SQL Command | Purpose |
| :--- | :--- | :--- |
| **Create** | `INSERT` | Adds new rows to a table. |
| **Read** | `SELECT` | Retrieves data from a table. |
| **Update** | `UPDATE` | Modifies existing data in a table. |
| **Delete** | `DELETE` | Removes data from a table. |

### Examples:
```
-- CREATE: Add a new user
INSERT INTO users (name, email, age)
VALUES ('Alice', 'alice@example.com', 25);

-- READ: Get all users older than 20
SELECT * FROM users WHERE age > 20;

-- UPDATE: Change Alice's email
UPDATE users
SET email = 'alice_new@example.com'
WHERE name = 'Alice';

-- DELETE: Remove Alice from the table
DELETE FROM users WHERE name = 'Alice';
```

## 2. Table Manipulation (DDL)
Data Definition Language (DDL) is used to define the structure of your database.

### Examples:
```
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    salary DECIMAL(10, 2),
    hire_date DATE
);

ALTER TABLE employees ADD COLUMN department VARCHAR(50);

DROP TABLE employees;
```

## 3. Filtering and Sorting
- These clauses help you refine your `SELECT` operations.
- DISTINCT: Removes duplicate results. `SELECT DISTINCT country FROM customers;`
- ORDER BY: Sorts the results (`ASC` is default, `DESC` for descending). `SELECT * FROM products ORDER BY price DESC;`
- LIMIT: Returns only a specific number of rows. `SELECT * FROM posts LIMIT 5;`
- LIKE: Pattern matching (`%` is a wildcard). `SELECT * FROM users WHERE name LIKE 'J%';` -- Finds Joe, Jane, etc.


## 4. Joins
- LEFT JOIN:  Keeps all rows from the first (left) table. If there's no match in the second table, you get NULL values for those columns.
- RIGHT JOIN: Keeps all rows from the second (right) table. If there's no match in the first table, you get NULL values for those columns.

- Ex: Imagine you have a Students table and an ID_Cards table.
    - Left: You get every student, including those who don't have an ID card yet (those students will show NULL for card info).
    - Right: You get every ID card, including any cards that aren't assigned to a student yet (those cards will show NULL for student info).

### 1. INNER JOIN (The Default)
Returns only the rows where there is a match in both tables. If a student isn't in a class, or a class has no students, they are excluded.
```
SELECT s.name, c.class_name
FROM students s
INNER JOIN classes c ON s.class_id = c.id;
```

### 2. LEFT JOIN (Left Outer Join)
Returns all rows from the left table, plus any matching rows from the right. If there’s no match on the right, you get NULL.
```
-- Shows all students, even those not enrolled in a class
SELECT s.name, c.class_name
FROM students s
LEFT JOIN classes c ON s.class_id = c.id;
```

### 3. RIGHT JOIN (Right Outer Join)
Returns all rows from the right table, plus any matching rows from the left. If there’s no match on the left, you get NULL.
```
-- Shows all classes, even those with zero students
SELECT s.name, c.class_name
FROM students s
RIGHT JOIN classes c ON s.class_id = c.id;
```

### 4. FULL OUTER JOIN 
Returns all rows from both tables. It matches them where possible and fills in NULL for everything else. This gives you the "total picture" of both datasets.
```
SELECT s.name, c.class_name
FROM students s
FULL OUTER JOIN classes c ON s.class_id = c.id;
```

### 5. CROSS JOIN (Cartesian Product)
Matches every single row from the first table with every single row of the second. There is no ON condition because it's a mathematical product ($Rows A \times Rows B$).
```
-- Creates a combination of every student with every possible class
SELECT s.name, c.class_name
FROM students s
CROSS JOIN classes c;
```

### 6. SELF JOIN
This is when you join a table to itself. It's extremely useful for hierarchical data, like finding which employee reports to which manager within a single Employees table.
```
-- Finding employee names and their managers
SELECT e.name AS Employee, m.name AS Manager
FROM employees e
JOIN employees m ON e.manager_id = m.id;
```
