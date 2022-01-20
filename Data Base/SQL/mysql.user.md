---
tags:
  - DB/SQL/DCL-Control/user
  - DB/SQL/Clients/mysql
date created: 2022-01-16 12:19
date updated: 2022-01-16 15:47
---

```sql
SELECT User, Host FROM mysql.user; 	-- список пользователей
-- +------------------+-----------+
-- | User             | Host      |
-- +------------------+-----------+
-- | mysql.infoschema | localhost |
-- | mysql.session    | localhost |
-- | mysql.sys        | localhost |
-- | root             | localhost |
-- +------------------+-----------+
-- 4 rows in set (0,00 sec)
```

```sql
Host		--	Хост пользователя (то есть: localhost,% и т. д.)
User		--	Имя пользователя (например: root, admin и т. д.)
Password		--	Пароль хранится как хешированное значение


-- ПРИВЕЛЕГИИ (Y или N)
-- CRUD
Select_priv
Insert_priv
Update_priv
Delete_priv
-- Defenition
Create_priv
Drop_priv
-- View
Repl_client_priv
Create_view_priv
Show_view_priv
-- 
Reload_priv
Shutdown_priv
Process_priv
File_priv
Grant_priv
References_priv
Index_priv
Alter_priv
Show_db_priv
Super_priv
Create_tmp_table_priv
Lock_tables_priv
Execute_priv
Repl_slave_priv
Create_routine_priv
Alter_routine_priv
Create_user_priv
Event_priv
Trigger_priv
Create_tablespace

-- БЕЗОПАСНОСТЬ
ssl_type
ssl_cipher	 -- (BLOB)
x509_issuer	 -- (BLOB)
x509_subject -- (BLOB)
plugin		
authentication_string

-- РЕСУРСЫ
max_questions		
max_updates			
max_connections		
max_user_connections


```

# Пример


