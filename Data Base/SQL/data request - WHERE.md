---
tags:
  - DB/SQL/DML-Manipulation/request
date created: 2021-12-16 11:42
date updated: 2022-01-10 12:42
---

**WHERE** - отфильтровать данные по нужному условию.

```sql
SELECT ...
FROM ... 
WHERE id_catalog > 2;



SELECT * FROM catalogs 
WHERE name = 'Процессоры';

select * from Customers
where City IN ('London', 'Berlin')
```

