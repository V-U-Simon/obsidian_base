---
tags:
  - Course
  - OS/linux
date created: 2021-11-13 15:34
date updated: 2021-11-21 13:26
---

## Содержание:

- [Список процессов в Linux](https://losst.ru/spisok-protsessov-linux#%D0%A1%D0%BF%D0%B8%D1%81%D0%BE%D0%BA_%D0%BF%D1%80%D0%BE%D1%86%D0%B5%D1%81%D1%81%D0%BE%D0%B2_%D0%B2_Linux)
  - [1. Утилита ps](https://losst.ru/spisok-protsessov-linux#1_%D0%A3%D1%82%D0%B8%D0%BB%D0%B8%D1%82%D0%B0_ps)
  - [2. Утилита top](https://losst.ru/spisok-protsessov-linux#2_%D0%A3%D1%82%D0%B8%D0%BB%D0%B8%D1%82%D0%B0_top)
  - [3. Утилита htop](https://losst.ru/spisok-protsessov-linux#3_%D0%A3%D1%82%D0%B8%D0%BB%D0%B8%D1%82%D0%B0_htop)
  - [4. Программа Gnome Monitor](https://losst.ru/spisok-protsessov-linux#4_%D0%9F%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B0_Gnome_Monitor)
  - [5. Утилита atop](https://losst.ru/spisok-protsessov-linux#5_%D0%A3%D1%82%D0%B8%D0%BB%D0%B8%D1%82%D0%B0_atop)
- [Выводы](https://losst.ru/spisok-protsessov-linux#%D0%92%D1%8B%D0%B2%D0%BE%D0%B4%D1%8B)

---

<https://losst.ru/komanda-source-v-linux> - **КОМАНДА SOURCE В LINUX**
<https://russianblogs.com/article/827430384/> - Глубокий анализ set, env, export, source, exec под Linux
<https://habr.com/ru/post/423049/> - Изучаем процессы в Linux
Содержание

1. [Введение](https://habr.com/ru/post/423049/#intro)
2. [Атрибуты процесса](https://habr.com/ru/post/423049/#definition)
3. [Жизненный цикл процесса](https://habr.com/ru/post/423049/#lifecycle)
   1. [Рождение процесса](https://habr.com/ru/post/423049/#fork)
   2. [Состояние «готов»](https://habr.com/ru/post/423049/#ready)
   3. [Состояние «выполняется»](https://habr.com/ru/post/423049/#running)
   4. [Перерождение в другую программу](https://habr.com/ru/post/423049/#exec)
   5. [Состояние «ожидает»](https://habr.com/ru/post/423049/#waiting)
   6. [Состояние «остановлен»](https://habr.com/ru/post/423049/#stopped)
   7. [Завершение процесса](https://habr.com/ru/post/423049/#exit)
   8. [Состояние «зомби»](https://habr.com/ru/post/423049/#zombie)
   9. [Забытье](https://habr.com/ru/post/423049/#wait)
