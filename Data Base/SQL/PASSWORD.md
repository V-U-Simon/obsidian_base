---
tags:
  - DB/SQL/DCL-Control/user
date created: 2022-01-16 12:19
date updated: 2022-01-16 12:30
---

```sql
SET PASSWORD 
	user_name =		-- если нет, то к текущему пользователю
	
    PASSWORD('text_password1');		-- обновить
	OLD_PASSWORD('text_password2');	-- сбросить
	'encrypted_password'; -- если уже был зашифрован
```

## Пример

```sql
SET PASSWORD 
	FOR 'samvel'@'localhost' =
	
	PASSWORD('klondike'); 		-- обновить
	OLD_PASSWORD('autumn'); 	-- сбросить
	-- Если новый пароль уже был зашифрован
	'*39C549BDECFBA8AFC3CE6B948C9359A0ECE08DE2'; 
```

# Источники:

- <https://oracleplsql.ru/change-a-user-password-mysql.html>