---
tags:
  - DB/SQL/DML-Manipulation/request
date created: 2021-12-16 11:42
date updated: 2022-01-09 21:13
---

**HAVING** - отфильтровать сгруппированную выборку (аналог [[data request - WHERE]])

```sql
-- ПРИМЕР
SELECT
  COUNT(*) AS total,
  SUBSTRING(birthday_at, 1, 3) AS decade
FROM
  users
GROUP BY
  decade
HAVING
  total >= 2;
```

## Запрос c WHERE и HAVING.

1. сначала фильтруется исходная таблица (пользователи по городам )
2. затем промежуточная таблица (количество клиентов не менее 5)

```sql
select City, count(CustomerID) as number_of_clients from Customers
WHERE CustomerName not in ('Around the Horn','Drachenblut Delikatessend')
group by City
HAVING number_of_clients >= 5
```

```ad-success
title: Можно использовать HAVING без группировки GROUP BY
В этом случае каждая строка таблицы рассматривается как отдельная группа.
```

> #todo/ask - зачем может понадобится истользовать having без группировки? - пример
