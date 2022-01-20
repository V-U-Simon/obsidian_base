---
tags:
  - Course
  - OS/linux
  - review
date created: 2021-11-13 15:34
---

# Как в Linux подключить новый диск, разметить и отформатировать разделы

- [Системное администрирование](https://zalinux.ru/?cat=31),
- [Утилиты](https://zalinux.ru/?cat=2),
- [Файловая система](https://zalinux.ru/?cat=20)
- [cfdisk](https://zalinux.ru/?tag=cfdisk),
- [ext2](https://zalinux.ru/?tag=ext2),
- [ext3](https://zalinux.ru/?tag=ext3),
- [ext4](https://zalinux.ru/?tag=ext4),
- [fdisk](https://zalinux.ru/?tag=fdisk),
- [fstab](https://zalinux.ru/?tag=fstab),
- [gdisk](https://zalinux.ru/?tag=gdisk),
- [lsblk](https://zalinux.ru/?tag=lsblk),
- [mount](https://zalinux.ru/?tag=mount),
- [NTFS](https://zalinux.ru/?tag=ntfs),
- [диски и устройства хранения данных](https://zalinux.ru/?tag=%d0%b4%d0%b8%d1%81%d0%ba%d0%b8-%d0%b8-%d1%83%d1%81%d1%82%d1%80%d0%be%d0%b9%d1%81%d1%82%d0%b2%d0%b0-%d1%85%d1%80%d0%b0%d0%bd%d0%b5%d0%bd%d0%b8%d1%8f-%d0%b4%d0%b0%d0%bd%d0%bd%d1%8b%d1%85),
- [права доступа к файлам (разрешения)](https://zalinux.ru/?tag=%d0%bf%d1%80%d0%b0%d0%b2%d0%b0-%d0%b4%d0%be%d1%81%d1%82%d1%83%d0%bf%d0%b0-%d0%ba-%d1%84%d0%b0%d0%b9%d0%bb%d0%b0%d0%bc-%d1%80%d0%b0%d0%b7%d1%80%d0%b5%d1%88%d0%b5%d0%bd%d0%b8%d1%8f),
- [разметка дисков](https://zalinux.ru/?tag=%d1%80%d0%b0%d0%b7%d0%bc%d0%b5%d1%82%d0%ba%d0%b0-%d0%b4%d0%b8%d1%81%d0%ba%d0%be%d0%b2),
- [файловые системы](https://zalinux.ru/?tag=%d1%84%d0%b0%d0%b9%d0%bb%d0%be%d0%b2%d1%8b%d0%b5-%d1%81%d0%b8%d1%81%d1%82%d0%b5%d0%bc%d1%8b),
- [форматирование](https://zalinux.ru/?tag=%d1%84%d0%be%d1%80%d0%bc%d0%b0%d1%82%d0%b8%d1%80%d0%be%d0%b2%d0%b0%d0%bd%d0%b8%d0%b5)

## Оглавление

- [1. Активация диска в Linux](https://zalinux.ru/?p=1798#1)
- [2. Как узнать имена дисков, как просмотреть все диски в системе](https://zalinux.ru/?p=1798#2)
- [3. Разметка дисков (разделение на разделы) в Linux](https://zalinux.ru/?p=1798#3)
- [4. Форматирование разделов](https://zalinux.ru/?p=1798#4)

[5. Монтирование и размонтирование дисков](https://zalinux.ru/?p=1798#5)

- [6. Автоматическое монтирование диска при загрузке Linux](https://zalinux.ru/?p=1798#6)
- [7. Подключение съёмного носителя (флешки, внешнего диска) в Linux](https://zalinux.ru/?p=1798#7)
- [8. Как просмотреть все диски и точки монтирования](https://zalinux.ru/?p=1798#8)
- [9. Как удалить разделы диска](https://zalinux.ru/?p=1798#9)
- [10. Перемонтирование диска с правами записи](https://zalinux.ru/?p=1798#10)
- [Заключение](https://zalinux.ru/?p=1798#11)
