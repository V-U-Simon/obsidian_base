---
tags:
  - DB/SQL/DCL-Control/user
  - DB/SQL/DCL-Control/connection
date created: 2022-01-16 12:19
date updated: 2022-01-16 12:33
---

```sql
DROP USER user_name;
```

`DROP USER` - не закрывает соединение удаляемого пользователя (сможет работать с БД, пока не закроется соединение с сервером)


## Пример

```sql
-- удаление нескольких пользователей
DROP USER 'samvel'@'localhost', 'serg'@'localhost';
```

