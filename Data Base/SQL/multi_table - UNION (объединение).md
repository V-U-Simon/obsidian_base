---
tags:
  - DB/SQL/DML-Manipulation/request
date created: 2021-12-16 11:42
date updated: 2022-01-10 11:23
---

**UNION** используется для добавления данных в таблицу (некий аналог [[INSERT]]).

- по умолчанию показывает уникальные строки.
- колличество столбцов и их тип должны совподать
- довольно медленная команда
- промежуточный результат размещается на жестком диске


```sql
SELECT col_1, col_N
FROM tables
UNION
SELECT col_1, col_N
FROM tables
```

## Пример

```sql
SELECT supplier_id
FROM suppliers
UNION ALL 			  -- Отменяет выдачу уникальных значений (Выводить дубли)
SELECT supplier_id
FROM order_details
ORDER BY supplier_id -- сортирует полученную выборку
LIMIT 10; 			 -- ограничит размер выборки
-- возвращает одно поле из нескольких SELECT 
```

- для фильтрации [[SELECT]] нужно использовать [[multi_table - SELECT (subquery)|вложенные запросы]]