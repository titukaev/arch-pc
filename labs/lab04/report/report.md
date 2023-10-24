---
## Front matter
title: "Отчёта по лабораторной работе 4"
subtitle: "Создание и процесс обработки программ на языке ассемблера NASM"
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

Целью работы является освоение процедуры компиляции и сборки программ, написанных на ассемблере NASM.

# Выполнение лабораторной работы

1. Создаю каталог lab04 командой mkdir, перехожу в него с помощью команды cd, создаю файл hello.asm.

![Создание каталога и файла](image/01.png){ #fig:001 width=70%, height=70% }

2. Открыл файл и написал код программы по заданию.

![Программа в файле hello.asm](image/02.png){ #fig:002 width=70%, height=70% }

Также размещаю код программы в отчете.

```
SECTION .data
hello: DB 'Hello world!',10 
helloLen: EQU $-hello
SECTION .text
GLOBAL _start
_start:
mov eax,4
mov ebx,1
mov ecx,hello
mov edx,helloLen
int 80h
mov eax,1
mov ebx,0
int 80h
```
3. Транслировал файл командой nasm. Получился объектный файл hello.o

4. Транслировал файл командой nasm с дополнительными опциями. 
Получился файл листинга list.lst, объектный файл obj.o, в программу добавилась отладочная информация.

5. Выполнил линковку командой ld и получил исполняемый файл.

6. Еще раз выполнил линковку для объектного файла obj.o и получил исполняемый файл main.

7. Запустил исполняемые файлы.

![Трансляция, линковка и запуск программы](image/03.png){ #fig:003 width=70%, height=70% }

8. Изменил сообщение Hello world на свое имя и запустил файл еще раз.

![Программа в файле lab4.asm](image/04.png){ #fig:004 width=70%, height=70% }

Также размещаю код программы в отчете.

```
SECTION .data
hello: DB 'Тимур Тукаев',10 
helloLen: EQU $-hello
SECTION .text
GLOBAL _start
_start:
mov eax,4
mov ebx,1
mov ecx,hello
mov edx,helloLen
int 80h
mov eax,1
mov ebx,0
int 80h
```

![Сборка и проверка программы lab4.asm](image/05.png){ #fig:005 width=70%, height=70% }

# Выводы

Освоили процесс компиляции и сборки программ, написанных на ассемблере nasm.
