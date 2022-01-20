---
tags:
  - DB/SQL/DML-Manipulation/request
date created: 2021-12-16 11:42
date updated: 2022-01-06 22:22
---

```sql
-- ШАБЛОНЫ
LIKE	    -- Соответствие шаблону 
-- % 	- любое колличество символов либо их отсутвие
-- _ 	- один символ


RLIKE, REGEXP -- Поиск через регулярные выражения
```

### LIKE

```sql
SELECT * FROM tb_name
   WHERE name 
   LIKE '%o'; -- все значения которые заканчиваюстя на 'o'

```

### RLIKE / REGEXP - [[Regular expression|Регулярные выражения]]

- [[re - Генераторы регулярных выражений]]
- [[Основы синтаксиса]]

```sql
-- пример регулярного выражения 
SELECT '323.43'
RLIKE '^[0-9]*\\.[0-9]{2}& AS '323.43'; 
```