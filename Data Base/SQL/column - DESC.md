---
tags:
  - DB/SQL/DDL-Defenition/column
date created: 2021-12-16 11:42
date updated: 2022-01-04 17:52
---

```sql
DESC     tb_name -- выводит описание и тип стобцов в талице
DESCRIBE tb_name -- более длинная версиятолько в mysql



-- +---------------+-----------------+------+-----+---------+----------------+
-- | Field         | Type            | Null | Key | Default | Extra          |
-- +---------------+-----------------+------+-----+---------+----------------+
-- | id            | bigint unsigned | NO   | PRI | NULL    | auto_increment |
-- | firstname     | varchar(100)    | YES  | MUL | NULL    |                |
-- | lastname      | varchar(100)    | YES  |     | NULL    |                |
-- | email         | varchar(100)    | YES  | UNI | NULL    |                |
-- | password_hash | varchar(100)    | YES  |     | NULL    |                |
-- | phone         | bigint          | YES  |     | NULL    |                |
-- | is_deleted    | bit(1)          | YES  |     | b'0'    |                |
-- +---------------+-----------------+------+-----+---------+----------------+

```
