---
tags:
  - DB/SQL/DML-Manipulation/request
date created: 2021-12-16 11:42
date updated: 2022-01-06 23:25
---

**WITH ROLLUP** - добавляет еще одну строку с суммой значений всех предыдущих строк.

```sql
WITH ROLLUP  -- подсчитывает все отображаемые резльататы столбоц

-- Пример
SELECT gender, COUNT(gender)
FROM profiles
GROUP BY gender
WITH ROLLUP;

-- +--------+---------------+
-- | gender | COUNT(gender) |
-- +--------+---------------+
-- | f      |             3 |
-- | m      |             7 |
-- | NULL   |            10 |
-- +--------+---------------+
```
