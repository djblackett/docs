---
Title: "Primary Keys"
Subjects:
  - "Computer Science"
  - "Data Science"
Tags: 
  - "Comments"
  - "Documentation"
Catalog Content:
  - "https://www.codecademy.com/learn/learn-sql"
  - "https://www.codecademy.com/learn/paths/computer-science"
  - "https://www.codecademy.com/learn/paths/data-science"
---

SQL tables sometimes has a column that uniquely identifies each row of that table. These special columns are called *primary keys*.

Primary key column has a few requirements:

- None of the values can be `NULL`.
- Each value must be unique (i.e., you can’t have two customers with the same `customer_id` in the `customers` table).
- A table can not have more than one primary key column.

## Syntax

 `PRIMARY KEY` columns can be used to uniquely identify the row. Attempts to insert a row with an identical value to a row already in the table will result in a *constraint violation* which will not allow you to insert the new row.

The statement below sets a `PRIMARY KEY` on the `students` table:

```sql
CREATE TABLE students (
  id INTEGER PRIMARY KEY, 
  name TEXT,
  grade INTEGER,
  age INTEGER
);
```

## Foreign Keys

When the primary key for one table appears in a different table, it is called a *foreign key*.

Why is this important? The most common types of joins will be joining a foreign key from one table with the primary key from another table. For instance, when we join the `orders` table and the `customers` table, we join on the `customer_id` column, which is a foreign key in `orders` and the primary key in `customers`.

**Note:** There can be only one `PRIMARY KEY` column per table and multiple `UNIQUE` columns.