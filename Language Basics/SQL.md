#technical 

## Overview

### General Tips
- SQL doesn't _require_ you to write the keywords all capitalized, but as a convention, it helps people distinguish SQL keywords from column and tables names, and makes the query easier to read.

### Glossary

| Term     | Definition                                                                                                                                           |
| -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| query    | A statement which declares what data we are looking for, where to find it in the database, and optionally, how to transform it before it is returned |
| instance | row in a table                                                                                                                                       |


---
## `SELECT` Queries

The most basic query requires column name(s) and the table from where to get them from:

```sql
SELECT column1, column2, ...
FROM mytable;
```

### `SELECT *` (all)

Use `*` to select all columns in a table

```sql
SELECT *
FROM mytable;
```

---
## `WHERE` Constraints

Use `WHERE` to apply constrains to your query. The conditions can be chained using `AND/OR`.

```sql
SELECT col1, col2, ...
FROM mytable
WHERE col condition AND/OR col condition
```

### Logical Operators

| Operation             | Function                                             |
| --------------------- | ---------------------------------------------------- |
| `=, !=, <, <=, >=, >` | Numerical op                                         |
| `BETWEEN...AND...`    | Number is within range of two values (inclusive)     |
| `NOT BETWEEN…AND…`    | Number is not within range of two values (inclusive) |
| `IN (list)`           | Number exists in a list                              |
| `NOT IN (list)`       | Number does not exist in a list                      |

todo: https://sqlbolt.com/lesson/select_queries_with_constraints_pt_2

---
##