---
tags:
  - DB/SQL/DDL-Defenition/table
date created: 2021-12-16 11:41
date updated: 2022-01-03 18:52
---

```sql
TRUNCATE tb;	-- удаляет + обнуляет счетчик
-- не допускает условного удаления

-- Равносилен:
DROP TABLE tb_name; 
CREATE TABLE tb_name ...
```
 