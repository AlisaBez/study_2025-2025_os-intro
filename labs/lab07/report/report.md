---
## Front matter
title: "Лабораторная работа №7"
subtitle: "дисциплина: Архитектура компьютера"
author: "Безходарнова Алиса Викторовна"

## Generic options
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
  - spelling=modern
  - babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---
# Цель работы

Ознакомление с файловой системой Linux, её структурой, именами и содержанием каталогов. Приобретение практических навыков по применению команд для работы с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы

# Задание

Выполнить лабораторную работу по указаниям.

# Теоретическое введение

Файловая система в Linux состоит из фалов и каталогов. Каждому физическому носи- телю соответствует своя файловая система. Существует несколько типов файловых систем. Перечислим наиболее часто встречаю- щиеся типы: – ext2fs (second extended filesystem); – ext2fs (third extended file system); – ext4 (fourth extended file system); – ReiserFS; – xfs; – fat (file allocation table); – ntfs (new technology file system). Для просмотра используемых в операционной системе файловых систем можно вос- пользоваться командой mount без параметров.

# Выполнение лабораторной работы

Сначала копирую файл, затем создаю новый каталог, в который перемещаю скопированный файл. (рис. -@fig:001).

![Копирование файла](image/1.jpg){#fig:001 width=70%}

Cоздаю новый файл копирую туда файл и переименовываю его (рис. -@fig:002).

![Создание файла](image/2.jpg){#fig:002 width=70%}

Cоздаю новый каталог и перемещаю его и перименовываю (Рис -@fig:003).

![Перемещение файла](image/3.jpg){#fig:003 width=70%}

Определяю опции команды chmod (Рис -@fig:004)

![сhmod](image/4.jpg){#fig:004 width=70%}

Промастриваю содержимое файла password (Рис -@fig:005)

![password](image/5.jpg){#fig:005 width=70%}

Копирую и перемещаю файлы (Рис -@fig:006)

![Копирование и перемещение](image/6.jpg){#fig:006 width=70%}

Лишаю файлов права на чтение, и смотрю, что получается. При лишение прав, система не дает к ним доступа (Рис -@fig:007)

![Лишение доступа](image/10.jpg)){#fig:007 width=70}

Командой man читаю команды (Рис -@fig:008)

![man fsck](image/7.jpg){#fig:008 width=70%}

И (Рис -@fig:009)

![man mkfs](image/9.jpg){#fig:009 width=70%}

И (Рис -@fig:010)

![man kill](image/8.jpg){#fig:010 width=70%}

# Вывод

В ходе данной лабораторной работы я ознакомилась с файловой системой Linux, ее структурой именами и содержанием каталогов.

# Контрольные вопросы

1. Дайте характеристику каждой файловой системе, существующей на жёстком диске компьютера, на котором вы выполняли лабораторную работу.
В Fedora Sway на виртуальной машине файловая система жёсткого диска — ext4 (основная), также может быть swap (раздел подкачки), vfat (для EFI-раздела) и tmpfs (временные файловые системы в памяти). Точный список можно посмотреть командами df -T или lsblk -f.

2. Приведите общую структуру файловой системы и дайте характеристику каждой директории первого уровня этой структуры.
/ — корень.
/bin — основные команды.
/boot — загрузчик и ядро.
/dev — файлы устройств.
/etc — конфигурации.
/home — домашние папки пользователей.
/lib — библиотеки.
/media, /mnt — точки монтирования.
/opt — дополнительное ПО.
/proc, /sys — виртуальные файловые системы.
/root — домашняя папка root.
/sbin — системные команды.
/tmp — временные файлы.
/usr — пользовательские программы.
/var — переменные данные (логи, очереди).

3. Какая операция должна быть выполнена, чтобы содержимое некоторой файловой системы было доступно операционной системе?
Операция монтирования (команда mount).

4. Назовите основные причины нарушения целостности файловой системы. Как устранить повреждения файловой системы?
Причины: отключение питания, сбой ПО, ошибки диска. Устранение: fsck.

5. Как создаётся файловая система?
С помощью команды mkfs -t тип /dev/устройство.

6. Дайте характеристику командам для просмотра текстовых файлов.
cat — выводит весь файл, less — постраничный просмотр, head/tail — вывод начала или конца файла.

7. Приведите основные возможности команды cp в Linux.
Копирование файлов и каталогов (с опцией -r), запрос подтверждения перезаписи (-i).

8. Приведите основные возможности команды mv в Linux.
Перемещение и переименование файлов и каталогов.

9. Что такое права доступа? Как они могут быть изменены?
Права доступа — это правила чтения, записи и выполнения для владельца, группы и остальных. Изменяются командой chmod.

# Список литературы{.unnumbered}
