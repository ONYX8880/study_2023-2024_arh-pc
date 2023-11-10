---
## Front matter
title: "ОТЧЕТ ПО ЛАБОРАТОРНОЙ РАБОТЕ № 5"
subtitle: "дисциплина:	Архитектура компьютера"
author: "Газизянов Владислав Альбертович"

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
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Освоить инструкции языка ассемблера mov.Приобрести знания использования Midnight Commander.

# Задание

Написать 2 программы по примеру и изменить их структуру по условию.

# Выполнение лабораторной работы

## Порядок выполнения лабораторной работы

Открываем Mid. Commander 

<p align="center">![mc](image/Снимок экрана от 2023-11-09 23-43-46.png){#fig:001 width=70%}</p>

Переходим в каталог, созданный при выполнении 4 ЛБ 

<p align="center">![Переходим в каталог](image/Снимок экрана от 2023-11-09 23-45-21.png){#fig:002 width=70%}</p>

Создаем каталог lab05 

<p align="center">![Создаем каталог ](image/Снимок экрана от 2023-11-09 23-45-49.png){#fig:003 width=70%}</p>

Создаем файл lab5-1.asm 

<p align="center">![touch](image/Снимок экрана от 2023-11-09 23-49-31.png){#fig:004 width=70%}</p>

Открываем файл для редактирования и заполняем его по листингу 

<p align="center">![Открывем файл, заполняем](image/Снимок экрана от 2023-11-09 23-53-21.png){#fig:005 width=70%}</p>

Открывем файл и просматриваем 

<p align="center">![Открываем файл и убеждаемся, что файл содержит текст программы](image/Снимок экрана от 2023-11-09 23-54-23.png){#fig:006 width=70%}</p>

Транслируем текст программы и запускаем файл 

<p align="center">![Проверка](image/Снимок экрана от 2023-11-09 23-58-07.png){#fig:007 width=70%}</p>

Скачиваем файл  

<p align="center">![Скачиваем файл](image/Снимок экрана от 2023-11-10 12-21-46.png){#fig:008 width=70%}</p>

Копируем файл в нужную директорию 

<p align="center">![Копируем файл](image/Снимок экрана от 2023-11-10 12-23-38.png){#fig:009 width=70%}</p>

Создаем копию файла 

<p align="center">![Создаем копию файла ](image/Снимок экрана от 2023-11-10 00-06-29.png){#fig:010 width=70%}</p>

Проверяем созданный файл 

<p align="center">![Проверяем скопировался ли файл](image/Снимок экрана от 2023-11-10 00-11-54.png){#fig:011 width=70%}</p>

Открываем новый файл и заполняем его  

<p align="center">![Открываем и заполняем файл](image/Снимок экрана от 2023-11-10 12-25-55.png){#fig:012 width=70%}</p>

Открываем файл для редактирования и меняем sprintLF на sprint

<p align="center">![Редактируем файл](image/Снимок экрана от 2023-11-10 12-08-26.png){#fig:014 width=70%}</p>

Транслируем и запускаем файл

<p align="center">![Смотрим, как работает программа и сравниваем с прошлой ](image/Снимок экрана от 2023-11-10 12-13-44.png){#fig:015 width=70%}</p>


## Задание для самостоятельной работы

Создаем копию файла lab5-1.asm 

<p align="center">![Создаем копию файла lab5-1.asm](image/Снимок экрана от 2023-11-10 22-39-02.png){#fig:016 width=70%}</p>

Редактируем файл, чтобы введеный текст с клавиатуры выводился в консоль 

<p align="center">![Редактируем файл](image/Снимок экрана от 2023-11-10 22-42-16.png){#fig:017 width=70%}</p>

Транслируем файл и запускаем программу 

<p align="center">![Проверяем правильность](image/Снимок экрана от 2023-11-10 22-43-54.png){#fig:018 width=70%}</p>

Создаем копию файла lab5-2.asm 

<p align="center">![Создаем копию файла lab5-2.asm](image/Снимок экрана от 2023-11-10 22-51-28.png){#fig:019 width=70%}</p>

Редактируем файл, чтобы введеный текст с клавиатуры выводился в консоль 

<p align="center">![Редактируем файл](image/Снимок экрана от 2023-11-10 22-47-42.png){#fig:020 width=70%}</p>

Транслируем файл и запускаем 

<p align="center">![Проверяем правильность программы](image/Снимок экрана от 2023-11-10 22-48-39.png){#fig:021 width=70%}</p>

# Выводы

Мы приобрели навыки работы с Midnight Commander и осоили инструкции mov.
