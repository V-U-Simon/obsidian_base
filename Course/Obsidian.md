---
tags:
  - Course/cheatsheet
  - Course/obsidian
date created: 2021-11-13 22:02
---

Программа для ведения заметок/каталогов. Основной язык Markdown

## Hotkeys

```
cmnd + o	# открытие - путь к заметке
cmnd + p 	# команды для выполнения 
cmnd + e 	# просмотр/редактирование 
cmnd + r 	# правая панель
cmnd + l	# левая панель
```

## PrettyLiner

должен приводить форматирование к общему виду и добавляет даты и тэги при создании и обновлении

```shell
cmnd + opt + L # Только на руссской раскладке работает


# new header
tags:
  - review

sr-due: '{{date:YYYY-MM-DD}}'
sr-interval: 1
sr-ease: 170

date created: "{{date:YYYY-MM-DD HH:mm}}" 

# update shell
tags:
  - review


date updated: "{{date:YYYY-MM-DD HH:mm}}" 
```

## admonition
[Документация](https://squidfunk.github.io/mkdocs-material/reference/admonitions/)
code
````ad-warning
title: The code is inside a card
```python
print('some_text')
```
````

- <icons <http://nagoshiashumari.github.io/Rpg-Awesome/>

```ad-note
title: Nested Admonitions
icon: hourglass
collapse: open

!!! ad-danger
	title: This admonition is nested.
	collapse: close
	This is a nested admonition!
	
	!!! ad-warning
		title: This admonition is closed.



This is in the original admonition.
```

```
!!! ad-<type> ""

content

--- admonition
```

## Spaces repetition (foldersnote)

```
side1::side2
side1:::side2 == side1::side2, side2::side1

side1
?
side2

side2
??
side1

open_text ==close_text== 	# open_text ...
```


## flashcards

[Описание](https://user-images.githubusercontent.com/43380836/115256965-5d455f00-a138-11eb-988f-27ba29f328a0.mp4)

## icons



- [ ] как добавлять иконки #todo

## templator

[документация на git](https://github.com/SilentVoid13/Templater)

## Dataview


```dataview
LIST
FROM #linux/accounts/user
sort file.name
```
пример
### Добавиление методанных:

- в заголовок

  ```
   ---
   alias: "document"
   last-reviewed: 2021-08-17
   thoughts:
     rating: 8
     reviewable: false
   ---
  ```

`alias` - нужен для возможности добавления обратных ссылок

- в саму заметку

  ```
    Basic Field:: Value
    **Bold Field**:: Nice!
  ```

## Источники:

- [Zettelkasten и Obsidian — лучшие друзья вашей памяти и креативности](https://habr.com/ru/post/548154/)
- [youtube_канал_об_obsidian](https://www.youtube.com/c/qnnnp/videos)
- [DataView](https://github.com/blacksmithgu/obsidian-dataview)