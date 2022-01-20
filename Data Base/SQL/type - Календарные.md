---
tags:
  - DB/SQL/DDL-Defenition/column
date created: 2021-12-16 16:53
date updated: 2022-01-08 13:01
---

```sql
DATE      -- ГГГГ-ММ-ДД
DATETIME  -- ГГГГ-ММ-ДД ЧЧ:ММ:СС (обновляется при создании и обновлении)
TIMESTAMP -- ГГГГ-ММ-ДД ЧЧ:ММ:СС (от 1970 года до 2038)
TIME      --            ЧЧ:ММ:СС
YEAR      -- ГГГГ

-- Пример добавления нового стобца
updated_at DATE DEFAULT NOW() ON UPDATE NOW(),
```

## Предельные значения

```sql
DATE  	 | '1000-01-01' до '9999-12-31'
DATETIME | '1000-01-01 00:00:00' до '9999-12-31 23:59:59'
TIME	 | '-838:59:59' до '838:59:59'
```

## Источники:

- [отличие типов данных DATETIME и TIMESTAMP](https://habr.com/ru/post/61391/)
