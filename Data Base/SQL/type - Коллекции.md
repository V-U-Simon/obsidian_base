---
tags:
  - DB/SQL/DDL-Defenition/column
date created: 2021-12-16 17:32
---

позволяют сохранять множество значений или даже целые документы в виде JSON-полей

элементы множеств сохраняются в виде чисел

```sql
-- Может принимать
ENUM -- одно значение из списка
SET  -- комбинацию заданных значений

JSON --
```

```sql
INSERT INTO tbl VALUES(1, '{"first": "Hello", "second": "World"}');
SELECT * FROM tbl;
SELECT collect->>"$.first" FROM tbl;
SELECT collect->>"$.second" FROM tbl;
```
