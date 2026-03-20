---
## Front matter
title: "Лабораторная работа №6"
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

Приобретение практических навыков взаимодействия пользователя с системой посредством командной строки.

# Задание

Выполнить лабораторную работу по указаниям.

# Теоретическое введение

Приобретение практических навыков взаимодействия пользователя с системой по-
средством командной строки.

# Выполнение лабораторной работы

Определяю имя домашнего каталога. (рис. -@fig:001).

![Домашний каталог](image/1.jpg){#fig:001 width=70%}

Перехожу в каталог tmp (рис. -@fig:002).

![Каталог](image/2.jpg){#fig:002 width=70%}

Иcпользую команду ls с разными опциями (Рис -@fig:003).

![ls -la](image/4.jpg){#fig:003 width=70%}

И (Рис -@fig:004)

![ls -a](image/5.jpg){#fig:004 width=70%}

И (Рис -@fig:005)

![ls -h, ls -f](image/6.jpg){#fig:005 width=70%}

Проверяю есть ли подкатолог и убеждаюсь, что он есть (Рис -@fig:006)

![Проверка подкаталога](image/8.jpg){#fig:006 width=70%}

ВЫвожу на экран содержимое домашнего каталога (Рис -@fig:007)

![Содержимое домашнего каталога](image/9.jpg)){#fig:007 width=70}

Создание каталога newdir и morefun (Рис -@fig:008)

![Каталоги](image/10.jpg){#fig:008 width=70%}

Создааю три новых каталога и удаляю их (Рис -@fig:009)

![Слздание и удаление каталогов](image/11.jpg){#fig:009 width=70%}

Пробую удалить каталог командой rm, потом удаляю каталог правильной командой и убеждаюсь, что он удален (Рис -@fig:010)

![Удаление каталога](image/12.jpg){#fig:010 width=70%}

Определяю опцию (Рис -@fig:011)

![Определение опции](image/13.jpg){#fig:011 width=70%}

Использую команду man (Рис -@fig:012)

![man для cd](image/17.jpg){#fig:012 width=70%}

И (Рис -@fig:013)

![man для mkdir](image/18.jpg){#fig:013 width=70%}

Просматриваю историю (Рис -@fig:014)

![История](image/19.jpg){#fig:014 width=70%}

Меняю команды (Рис -@fig:015)

![Замена команд](image/20.jpg){fig:015 width=70%}

# Вывод

В ходе данной работы я  Приобрела практические навыки взаимодействия пользователя с системой посредством командной строки

# Контрольные вопросы

1. Командная строка — это интерфейс взаимодействия пользователя с операционной системой, где команды вводятся в текстовом виде. В Linux взаимодействие осуществляется через командные интерпретаторы (shell), такие как /bin/bash.

2. Команда pwd (print working directory) выводит абсолютный путь текущего каталога. Пример: pwd → /home/username

3. Команда ls -F отображает имена файлов с символами, указывающими тип: / для каталогов, * для исполняемых, @ для ссылок. Пример: ls -F

4.Для отображения скрытых файлов (начинающихся с точки) используется опция -a команды ls. Пример: ls -a или ls -la

5. Файлы удаляются командой rm, пустые каталоги — rmdir. Можно одной командой rm -r для рекурсивного удаления каталога с содержимым. Пример: rm file.txt, rmdir dir, rm -r dir

6. Команда history выводит список ранее выполненных команд с номерами. Пример: history

7. Используется конструкция !<номер>:s/что_меняем/на_что_меняем. Пример: !25:s/l/la/ заменит в команде №25 "l" на "la".

8. Несколько команд разделяются символом ;. Пример: cd /tmp; ls -l; pwd

9. Экранирование — это способ использования специальных символов как обычных с помощью обратного слеша \. Пример: echo \$HOME выведет $HOME, а не значение переменной.

10. Опция -l выводит подробную информацию: тип файла, права доступа, число ссылок, владельца, размер, дату последнего изменения и имя файла.

11. Относительный путь указывает положение файла относительно текущего каталога, абсолютный — от корня /. Пример: cd .. (относительный), cd /home/user (абсолютный).

12. Используется команда man (manual). Пример: man ls выведет руководство по команде ls.

13. Клавиша Tab служит для автоматического дополнения имён команд, файлов и каталогов.

# Список литературы{.unnumbered}
