---
## Front matter
title: "Отчёта по лабораторной работе 3"
subtitle: "Язык разметки Markdown"
author: "Тукаев Тимур Ильшатович НММбд-03-23"

## Generic otions
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
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
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

Целью работы является изучить идеологию и применение средств контроля версий. Приобрести практические навыки по работе с системой git.

# Выполнение лабораторной работы

Регистрируюсь на GitHub

![Прохожу регистрацию на GitHub](image/01.png){ #fig:001 width=70%, height=70% }

Нахожу шаблонный репозиторий и создаю из него свой.

![Нахожу шаблон репозитория и создаю из него свой](image/02.png){ #fig:002 width=70%, height=70% }

Установил программу Git

![Установка программы Git](image/03.png){ #fig:003 width=70%, height=70% }

Сначала сделаем предварительную конфигурацию git, создаю пользователя и ставлю параметры.

![ Избираю предварительную конфигурацию Git, создаю пользователя и задаю параметры](image/04.png){ #fig:004 width=70%, height=70% }

Далее создаю ключи для идентификации.

![Создаю идентификационный ключ](image/05.png){ #fig:005 width=70%, height=70% }

И добавляю ключ в профиль на GitHub

![Добавляю ключ в профиль на GitHub](image/06.png){ #fig:006 width=70%, height=70% }

Теперь я создаю рабочий каталог и клонирую туда репозиторий с гитхаба.

![Создание рабочего каталога](image/07.png){ #fig:007 width=70%, height=70% }

Создаю курс

![Создание курса](image/08.png){ #fig:008 width=70%, height=70% }

Отправляю в GitHub

![Отправка данных в GitHub](image/09.png){ #fig:009 width=70%, height=70% }

Вот что получилось

![Результат проделанной работы](image/10.png){ #fig:010 width=70%, height=70% }

Загружаю этот отчет на платформу GitHub.

![Загрузка отчета(результат) в GitHub](image/11.png){ #fig:011 width=70%, height=70% }

# Выводы

В ходе выполнения работы изучили работу с GitHub. Изучили синтаксис языка разметки Markdown, получили отчет из шаблона при помощи Makefile. 
