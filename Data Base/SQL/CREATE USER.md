---
tags:
  - DB/SQL/DCL-Control/user
date created: 2022-01-16 12:19
date updated: 2022-01-16 13:10
---

```sql
CREATE USER
	user_name					    -- имя учетной записи
	IDENTIFIED BY 'password_value'; -- если не указать - пустая строка
```

# Пример

```sql
CREATE USER foo; -- пользователь без пароля
CREATE 
	USER shop 
	IDENTIFIED WITH sha256_password BY 'pass'; -- с паролем
```
