---
tags:
  - DB/SQL/DML-Manipulation/CRUD/read
date created: 2021-12-16 11:41
date updated: 2022-01-06 19:32
---

**To see foreign key relationships of a table:**

```sql
SELECT
    TABLE_NAME,
    COLUMN_NAME,
    CONSTRAINT_NAME,
    REFERENCED_TABLE_NAME,
    REFERENCED_COLUMN_NAME
FROM
    INFORMATION_SCHEMA.KEY_COLUMN_USAGE
WHERE
	REFERENCED_TABLE_SCHEMA = 'db_name'
    AND REFERENCED_TABLE_NAME = 'table_name';
```

**To see foreign key relationships of a column:**

```sql
SELECT
    TABLE_NAME,
    COLUMN_NAME,
    CONSTRAINT_NAME,
    REFERENCED_TABLE_NAME,
    REFERENCED_COLUMN_NAME
FROM
    INFORMATION_SCHEMA.KEY_COLUMN_USAGE
WHERE
	REFERENCED_TABLE_SCHEMA = 'db_name'
    AND REFERENCED_TABLE_NAME = 'table_name'
    AND REFERENCED_COLUMN_NAME = 'column_name';
```

## Источник:

- <https://tableplus.com/blog/2018/08/mysql-how-to-see-foreign-key-relationship-of-a-table.html>
