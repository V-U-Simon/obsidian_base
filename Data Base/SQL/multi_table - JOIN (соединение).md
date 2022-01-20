---
tags:
  - DB/SQL/DML-Manipulation/request
date created: 2021-12-16 11:42
date updated: 2022-01-10 13:52
---

**JOIN** - для объединения таблиц по ключу (присутствует в обеих таблицах).

```sql
INNER JOIN	-- связать только совподающие строки
LEFT JOIN 	-- + несвязанные строки у предыдущей таблицы
RIGHT JOIN 	-- + несвязанные строки у следующей таблицы
OUTER JOIN, CROSS JOIN -- не поддерживается mysql

-- ПРИМЕР
SELECT p.name, p.price, p.name
FROM 
	catalogs AS c			-- к таблице "с" (оставть несвязанные строки)
LEFT JOIN					-- присоеденить 
	product AS p			-- таблицу p
ON	c.id = p.catalog_id;	-- те строки, где совпадает id
```

```sql
-- ФИЛЬТРАЦИЯ И СОПОСТАВЛЕНИЕ КЛЮЧЕЙ
WHERE c.id == p.catalog_id 	-- работает после соединения
-- фильтрует большую общую таблицу
ON c.id == p.catalog_id 	-- работает в момет соединения
-- промежуточная таблица получается небольшой 

USING -- ???????
```

![[Снимок экрана 2022-01-09 в 21.22.11.png]]

## ВЫБОРКА ПОЛЕЙ ИЗ НЕСКОЛЬКИХ ТАБЛИЦ

```sql
SELECT order_details.order_id, customers.customer_name
FROM customers
INNER JOIN order_details
ON customers.customer_id = order_details.customer_id
ORDER BY order_details.order_id;
```

- отображает поля order_id и customer_name
- где значение customer_id совпадает в таблице customers и order_details
- Результаты сортируются по полю order_details.order_id в порядке возрастания
