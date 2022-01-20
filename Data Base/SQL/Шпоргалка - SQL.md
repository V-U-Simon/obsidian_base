---
tags:
  - Course
  - DB/SQL
date created: 2021-12-16 14:43
date updated: 2021-12-16 14:45
---

## Содержание

- [Что такое SQL?](https://habr.com/ru/post/564390/#%D1%87%D1%82%D0%BE-%D1%82%D0%B0%D0%BA%D0%BE%D0%B5-sql)
	- [Почему SQL?](https://habr.com/ru/post/564390/#%D0%BF%D0%BE%D1%87%D0%B5%D0%BC%D1%83-sql)
	- [Процесс SQL](https://habr.com/ru/post/564390/#%D0%BF%D1%80%D0%BE%D1%86%D0%B5%D1%81%D1%81-sql)
	- [Команды SQL](https://habr.com/ru/post/564390/#%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D1%8B-sql)
	- [Что такое таблица?](https://habr.com/ru/post/564390/#%D1%87%D1%82%D0%BE-%D1%82%D0%B0%D0%BA%D0%BE%D0%B5-%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D0%B0)
	- [Что такое поле?](https://habr.com/ru/post/564390/#%D1%87%D1%82%D0%BE-%D1%82%D0%B0%D0%BA%D0%BE%D0%B5-%D0%BF%D0%BE%D0%BB%D0%B5)
	- [Что такое запись или строка?](https://habr.com/ru/post/564390/#%D1%87%D1%82%D0%BE-%D1%82%D0%B0%D0%BA%D0%BE%D0%B5-%D0%B7%D0%B0%D0%BF%D0%B8%D1%81%D1%8C-%D0%B8%D0%BB%D0%B8-%D1%81%D1%82%D1%80%D0%BE%D0%BA%D0%B0)
	- [Что такое колонка?](https://habr.com/ru/post/564390/#%D1%87%D1%82%D0%BE-%D1%82%D0%B0%D0%BA%D0%BE%D0%B5-%D0%BA%D0%BE%D0%BB%D0%BE%D0%BD%D0%BA%D0%B0)
	- [`Что такое NULL`?](https://habr.com/ru/post/564390/#%D1%87%D1%82%D0%BE-%D1%82%D0%B0%D0%BA%D0%BE%D0%B5-null)
	- [Ограничения](https://habr.com/ru/post/564390/#%D0%BE%D0%B3%D1%80%D0%B0%D0%BD%D0%B8%D1%87%D0%B5%D0%BD%D0%B8%D1%8F)
- [Целостность данных](https://habr.com/ru/post/564390/#%D1%86%D0%B5%D0%BB%D0%BE%D1%81%D1%82%D0%BD%D0%BE%D1%81%D1%82%D1%8C-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85)
- [Нормализация БД](https://habr.com/ru/post/564390/#%D0%BD%D0%BE%D1%80%D0%BC%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F-%D0%B1%D0%B4)
- [Синтаксис SQL](https://habr.com/ru/post/564390/#%D1%81%D0%B8%D0%BD%D1%82%D0%B0%D0%BA%D1%81%D0%B8%D1%81-sql)
- [Типы данных](https://habr.com/ru/post/564390/#%D1%82%D0%B8%D0%BF%D1%8B-%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85)
- [Операторы](https://habr.com/ru/post/564390/#%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80%D1%8B)
- [Выражения](https://habr.com/ru/post/564390/#%D0%B2%D1%8B%D1%80%D0%B0%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F)
- [Создание БД](https://habr.com/ru/post/564390/#%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D0%B1%D0%B4)
- [Удаление БД](https://habr.com/ru/post/564390/#%D1%83%D0%B4%D0%B0%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B1%D0%B4)
- [Выбор БД](https://habr.com/ru/post/564390/#%D0%B2%D1%8B%D0%B1%D0%BE%D1%80-%D0%B1%D0%B4)
- [Создание таблицы](https://habr.com/ru/post/564390/#%D1%81%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5-%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D1%8B)
- [Удаление таблицы](https://habr.com/ru/post/564390/#%D1%83%D0%B4%D0%B0%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D1%8B)
- [Добавление колонок](https://habr.com/ru/post/564390/#%D0%B4%D0%BE%D0%B1%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BA%D0%BE%D0%BB%D0%BE%D0%BD%D0%BE%D0%BA)
- [Выборка полей](https://habr.com/ru/post/564390/#%D0%B2%D1%8B%D0%B1%D0%BE%D1%80%D0%BA%D0%B0-%D0%BF%D0%BE%D0%BB%D0%B5%D0%B9)
- [`Предложение WHERE`](https://habr.com/ru/post/564390/#%D0%BF%D1%80%D0%B5%D0%B4%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5-where)
- [`Операторы AND` и `OR`](https://habr.com/ru/post/564390/#%D0%BA%D0%BE%D0%BD%D1%8A%D1%8E%D0%BA%D1%82%D0%B8%D0%B2%D0%BD%D1%8B%D0%B5-%D0%BE%D0%BF%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80%D1%8B-and-%D0%B8-or)
- [Обновление полей](https://habr.com/ru/post/564390/#%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BF%D0%BE%D0%BB%D0%B5%D0%B9)
- [Удаление записей](https://habr.com/ru/post/564390/#%D1%83%D0%B4%D0%B0%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B7%D0%B0%D0%BF%D0%B8%D1%81%D0%B5%D0%B9)
- [`Предложения LIKE` и `REGEX`](https://habr.com/ru/post/564390/#%D0%BF%D1%80%D0%B5%D0%B4%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F-like-%D0%B8-regexp)
- [`Предложение TOP`/`LIMIT`/`ROWNUM`](https://habr.com/ru/post/564390/#%D0%BF%D1%80%D0%B5%D0%B4%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5-toplimitrownum)
- [`Предложения ORDER BY` и `GROUP BY`](https://habr.com/ru/post/564390/#%D0%BF%D1%80%D0%B5%D0%B4%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D1%8F-order-by-%D0%B8-group-by)
- [`Ключевое слово DISTINCT`](https://habr.com/ru/post/564390/#%D0%BA%D0%BB%D1%8E%D1%87%D0%B5%D0%B2%D0%BE%D0%B5-%D1%81%D0%BB%D0%BE%D0%B2%D0%BE-distinct)
- [Соединения](https://habr.com/ru/post/564390/#%D1%81%D0%BE%D0%B5%D0%B4%D0%B8%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F)
- [`Предложение UNION`](https://habr.com/ru/post/564390/#%D0%BF%D1%80%D0%B5%D0%B4%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5-union)
- [`Предложение UNION ALL`](https://habr.com/ru/post/564390/#%D0%BF%D1%80%D0%B5%D0%B4%D0%BB%D0%BE%D0%B6%D0%B5%D0%BD%D0%B8%D0%B5-union-all)
- [Синонимы](https://habr.com/ru/post/564390/#%D1%81%D0%B8%D0%BD%D0%BE%D0%BD%D0%B8%D0%BC%D1%8B)
- [Индексы](https://habr.com/ru/post/564390/#%D0%B8%D0%BD%D0%B4%D0%B5%D0%BA%D1%81%D1%8B)
- [Обновление таблицы](https://habr.com/ru/post/564390/#%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D1%8B)
- [Очистка таблицы](https://habr.com/ru/post/564390/#%D0%BE%D1%87%D0%B8%D1%81%D1%82%D0%BA%D0%B0-%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D1%8B)
- [Представления](https://habr.com/ru/post/564390/#%D0%BF%D1%80%D0%B5%D0%B4%D1%81%D1%82%D0%B0%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D1%8F)
- [`HAVING`](https://habr.com/ru/post/564390/#having)
- [Транзакции](https://habr.com/ru/post/564390/#%D1%82%D1%80%D0%B0%D0%BD%D0%B7%D0%B0%D0%BA%D1%86%D0%B8%D0%B8)
- [Временные таблицы](https://habr.com/ru/post/564390/#%D0%B2%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D1%8B%D0%B5-%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D1%8B)
- [Клонирование таблицы](https://habr.com/ru/post/564390/#%D0%BA%D0%BB%D0%BE%D0%BD%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5-%D1%82%D0%B0%D0%B1%D0%BB%D0%B8%D1%86%D1%8B)
- [Подзапросы](https://habr.com/ru/post/564390/#%D0%BF%D0%BE%D0%B4%D0%B7%D0%B0%D0%BF%D1%80%D0%BE%D1%81%D1%8B)
- [Последовательности](https://habr.com/ru/post/564390/#%D0%BF%D0%BE%D1%81%D0%BB%D0%B5%D0%B4%D0%BE%D0%B2%D0%B0%D1%82%D0%B5%D0%BB%D1%8C%D0%BD%D0%BE%D1%81%D1%82%D0%B8)


## Источники:
- <https://habr.com/ru/post/564390/>
