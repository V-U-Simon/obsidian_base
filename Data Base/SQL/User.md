---
tags:
  - DB/SQL/DCL-Control/user
date created: 2022-01-16 12:19
date updated: 2022-01-16 15:57
---

```sql
'username'@'host' -- учетная запись
-- username - имя
-- host		- адрсе, с которого разрешено обращаться к серверу MySQL

-- Пример
'username'@'%' разрешает 'username' обращаться к серверу MySQL с ip
```

```sql
SELECT USER(); 			-- текущий пользователь
SELECT CURRENT_USER(); 	-- текущий пользователь


CREATE USER user_name 	-- создает пользователя (пароль - пустая строка)
DROP USER user_name;	-- удаляет пользователя
RENAME USER olb to new  -- переименования пользователя
SET PASSWORD user_name = PASSWORD('pass') -- изменения пароля
```

# Пример
