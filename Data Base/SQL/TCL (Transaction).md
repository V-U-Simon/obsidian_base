---
tags:
  - DB/SQL/DML-Manipulation/transaction
date created: 2021-11-13 17:48
---

**TCL (Transaction Control Language)** - группа операторов для управления транзакциями. 

**Транзакция** - команды (инструкции), которые успешно завершаются как единое целое (все изменения в БД *фиксируются* или *отменяются*)

# Основные команды

```sql
BEGIN	 TRANSACTION 	-- начало транзакции
COMMIT 	 TRANSACTION 	-- применяет транзакцию
ROLLBACK TRANSACTION 	-- откатывает изменения
SAVE 	 TRANSACTION 	-- промежуточная точка сохранения
SAVEPOINT name 	 		 	-- промежуточная точка сохранения

SET AUTOCOMMIT=0;
```
