---
tags:
  - DB/SQL/DML-Manipulation/request
  - DB/SQL/DML-Manipulation/CRUD/read
date created: 2021-12-16 11:42
date updated: 2022-01-10 13:03
---

Запросы:

- корелируемые - если подзапрос использует столбец из внешнего запроса
- строчные запросы - возвращают более одного столбца

```sql
SELECT * FROM tb_1
WHERE (catalog_id, 5079) IN (SELECT id, price
							 FROM tb_2) -- сравнивание по двух столбцам

SELECT AVG(price)
FROM (SELECT *				-- получаем многострочный результат
	  FROM products		
	  WHERE catalog_id = 1) -- таблицу отфильтрованую по условию 
	  AS prod; 				-- под именем prod
-- Иное решение
SELECT AVG(price)
FROM products		
WHERE catalog_id = 1;
```

> В чем разница у терминов?
>
> - вложенные запросы
> - ложные запросы
> - подзапросы (subquery)

```sql
SELECT
	col_id,
	(SELECT col_name
	 FROM tb_2) -- вложенный запрос
FROM tb_1
```

## Пример

```sql
select
     id, firstname, lastname,
	 
     (select hometown from profiles
     where user_id = users.id) as 'city',
	 
     (select `filename` from media 
      where id = (select photo_id from profiles 
                  where user_id = users.id)
     ) as 'avatar'
from
     users
where id in (1, 2, 3, 5);
```
