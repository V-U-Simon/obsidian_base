---
tags:
  - DB/SQL/Clients/mysql
date created: 2021-12-19 13:24
---
**Информационная схема** - универсальная структура данных совместимая с разными СУБД, *находящаяся в оперативной памяти*

```sql
SELECT * FROM INFORMATION_SCHEMA.SCHEMATA; -- список БД
-- INFORMATION_SCHEMA
-- является виртуальной 
-- располагается ТОЛЬКО в оперативной памяти 

-- невозможно выбрать БД INFORMATION_SCHEMA | USE, 
-- невозможно к таблицам применить INSERT, UPDATE и DELETE.
-- возможно только оператора SELECT


SELECT * FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'shop'; -- список таблиц
```

