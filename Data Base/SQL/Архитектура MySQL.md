---
tags:
  - DB/SQL/Clients/mysql
date created: 2021-12-06 23:16
date updated: 2021-12-07 22:31
---

```sql
SHOW databases;  		-- список database
SHOW tables FROM mysql;	-- список tables
DESCRIBE mysql.User;	-- columl
-- SHOW и DESCRIBE отличные от MySQL могут не поддерживать
```


**Архитектуру MySQL**

> cуществует множество форков этой базы данных: Percona, MariaDB

- ядро
- сама база данных и движки, которые реализуют тот или иной механизм баз данных

**MySQL построена по клиент-серверной технологии: **

- сервер хранит и обслуживает базы данных
- клиенты шлют ему запросы на языке SQL и получают в ответ результирующие таблицы с данными

## Встроенные БД

```sql
mysql				-- системная БД
information_schema	-- универсальное описание структуры данных для разных СУБД
performance_schema
sys   				-- для исследования параметров производительности
```

- [[mysql]]
- [[information_schema]]


## Физическое расположение БД

```sql
SHOW VARIABLES LIKE 'datadir';
-- +---------------+------------------------+
-- | Variable_name | Value                  |
-- +---------------+------------------------+
-- | datadir       | /usr/local/mysql/data/ |
-- +---------------+------------------------+
-- 1 row in set (0,01 sec)
```

^ioy53j



