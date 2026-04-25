---
## Front matter
title: "Лабораторная работа №11"
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

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором Emacs

# Задание

1. Ознакомиться с теоретическим материалом.
2. Ознакомиться с редактором emacs.
3. Выполнить упражнения.
4. Ответить на контрольные вопросы.

# Теоретическое введение

Буфер — объект, представляющий какой-либо текст. Буфер может содержать что угодно, например, результаты компиляции программы или встроенные подсказки. Практически всё взаимодействие с пользователем, в том числе интерактивное, происходит посредством буферов. Фрейм соответствует окну в обычном понимании этого слова. Каждый
фрейм содержит область вывода и одно или несколько окон Emacs. Окно — прямоугольная область фрейма, отображающая один из буферов.
Каждое окно имеет свою строку состояния, в которой выводится следующая информация: название буфера, его основной режим, изменялся ли текст буфера и как далеко вниз
по буферу расположен курсор. Каждый буфер находится только в одном из возможных основных режимов. Существующие основные режимы включают режим Fundamental (наименее специализированный), режим Text, режим Lisp, режим С, режим Texinfo и другие. Под второстепенными режимами понимается список режимов, которые включены в данный момент в буфере выбранного окна.

# Выполнение лабораторной работы

Открываю редактор, создаю файл и записываю туда текст.  (рис. -@fig:001).

![Набор текста](image/1.jpg){#fig:001 width=70%}

Вырезаю строчку и вставляю ее в конец файла (рис. -@fig:002).

![Работа со строкой](image/2.jpg){#fig:002 width=70%}

Выделяю облатсь текста и также вставляю ее в конец (Рис -@fig:003).

![Работа с текстом](image/3.jpg){#fig:003 width=70%}

Удаляю всю облсть с помощью клавиш (Рис -@fig:004)

![Изменение текста](image/4.jpg){#fig:004 width=70%}

Возвращаю все обратно (Рис -@fig:005)

![Возвращение](image/5.jpg){#fig:005 width=70%}

Делю фрейм на 4 части.

![Деление фрейма](image/7.jpg){#fig:006 width=70%}

В каждом новом окне пишу текст

![Текст](image/8.jpg){#fig:007 width=70%}

Выполняю поиск

![Поиск](image/9.jpg){#fig:008 width=70%}

# Вывод

В ходе данной лабораторной работы я познакомилась с операционной системой Linux и приобрела практические навыки работы с редактором Emacs.

# Контрольные вопросы

1. Кратко охарактеризуйте редактор emacs. - Emacs — мощный расширяемый текстовый редактор на языке Elisp, поддерживающий буферы, окна, фреймы и множество режимов.

2. Какие особенности данного редактора могут сделать его сложным для освоения новичком? - Нестандартные комбинации клавиш (C-, M-), отсутствие привычных Ctrl+C/Ctrl+V, большое количество команд, непривычная терминология.

3. Своими словами опишите, что такое буфер и окно в терминологии emacs’а. - Буфер — это область памяти, содержащая текст (файл, справку, сообщение). Окно — прямоугольная область на экране, в которой отображается один из буферов.

4. Можно ли открыть больше 10 буферов в одном окне? - Да, можно. В одном окне одновременно виден только один буфер, но переключаться между буферами можно в любом количестве.

5. Какие буферы создаются по умолчанию при запуске emacs? - scratch, Messages, GNU Emacs.

6. Какие клавиши вы нажмёте, чтобы ввести следующую комбинацию C-c | и C-c C-|? - C-c |: Ctrl+C, затем Shift+\. C-c C-|: Ctrl+C, затем Ctrl+Shift+\.

7. Как поделить текущее окно на две части? - C-x 2 (горизонтально) или C-x 3 (вертикально).

8. В каком файле хранятся настройки редактора emacs? - ~/.emacs или ~/.emacs.d/init.el.

9. Какую функцию выполняет клавиша <- (стрелка влево) и можно ли её переназначить? - Стрелка влево перемещает курсор на один символ влево. Да, можно переназначить через global-set-key или define-key.

10. Какой редактор вам показался удобнее в работе vi или emacs? Поясните почему. - Emacs удобнее, потому что он немодальный (не нужно переключать режимы), имеет удобную работу с буферами и окнами, встроенную справку и легко расширяется.

# Список литературы{.unnumbered}
