---
## Front matter
title: "Отчёта по лабораторной работе №8"
subtitle: "Команды безусловного и условного переходов в Nasm. Программирование ветвлений."
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

Изучить работу циклов и обработкой аргументов командной строки.

# Задание

Написать программы с использованием циклов и обработкой аргументов командной строки.

# Выполнение лабораторной работы

Создаем каталог для программ ЛБ8, и в нем создаем файл
<p align="center">![Создание каталога](image/Снимок экрана от 2023-12-02 16-25-00.png){#fig:001 width=70%}</p>

Заполняем его в соответствии с листингом 8.1
<p align="center">![Заплнение 8.1](image/Снимок экрана от 2023-12-02 16-26-32.png){#fig:001 width=70%}</p>
Создаем исполняемый файл и запускаем его
<p align="center">![Проверка](image/Снимок экрана от 2023-12-02 16-31-13.png){#fig:001 width=70%}</p>

Снова открываем файл для редактирования и изменяем его, добавив изменение значения регистра в цикле
<p align="center">![Вносим изменения](image/Снимок экрана от 2023-12-02 16-31-58.png){#fig:001 width=70%}</p>

Создаем исполняемый файл и запускаем его
<p align="center">![Проверка](image/Снимок экрана от 2023-12-02 16-33-01.png){#fig:001 width=70%}</p>
Регистр ecx принимает значения, в цикле label данный регистр уменьшается на 2 командой sub и loop).
Число проходов цикла не соответсвует числу N, так как уменьшается на 2.
Снова открываем файл для редактирования и изменяем его, чтобы все корректно работало
<p align="center">![Редактирование](image/Снимок экрана от 2023-12-02 16-33-41.png){#fig:001 width=70%}</p>

Создаем исполняемый файл и запускаем его
<p align="center">![Проверка работы](image/Снимок экрана от 2023-12-02 16-31-13.png){#fig:001 width=70%}</p>
В данном случае число проходов цикла равна числу N.

Создаем новый файл
<p align="center">![Новый файл](image/Снимок экрана от 2023-12-02 16-38-27.png){#fig:001 width=70%}</p>

Заполняем его в соответствии с листингом 8.2
<p align="center">![Заполняем 8.2](image/Снимок экрана от 2023-12-02 16-36-26.png){#fig:001 width=70%}</p>
Создаем исполняемый файл и проверяем его работу, указав аргументы
<p align="center">![Проверка](image/Снимок экрана от 2023-12-02 16-38-37.png){#fig:001 width=70%}</p>
Програмой было обработано 3 аргумента.

Создаем новый файл lab8-3.asm
<p align="center">![Новый файл](image/Снимок экрана от 2023-12-02 16-40-14.png){#fig:001 width=70%}</p>

Открываем файл и заполняем его в соответствии с листингом 8.3
<p align="center">![Заполнение 8.3](image/Снимок экрана от 2023-12-02 16-40-56.png){#fig:001 width=70%}</p>

Создаём исполняемый файл и запускаем его, указав аргументы
<p align="center">![Проверка](image/Снимок экрана от 2023-12-02 16-42-08.png){#fig:001 width=70%}</p>

Снова открываем файл для редактирования и изменяем его, чтобы вычислялось произведение вводимых значений
<p align="center">![Редактирование](image/Снимок экрана от 2023-12-02 16-43-32.png){#fig:001 width=70%}</p>

Создаём исполняемый файл и запускаем его, указав аргументы
<p align="center">![Проверка работы](image/Снимок экрана от 2023-12-02 16-44-27.png){#fig:001 width=70%}</p>

## Самостоятельная работа
Вариант 2
Напишите программу, которая находит сумму значений функции f(x) для x = x1, x2, …, xn, т.е. программа должна выводить значение f(x1) + f(x2) + … + f(xn). Значения xi передаются как аргументы. Вид функции f(x) выбрать из таблицы 8.1 вариантов заданий в соответствии с вариантом, полученным при выполнении лабораторной работы № 7. Создайте исполняемый файл и проверьте его работу на нескольких наборах x = x1, x2, …, xn.
Создаем новый файл
<p align="center">![Новый файл](image/Снимок экрана от 2023-12-02 16-55-56.png){#fig:001 width=70%}</p>
Открываем его и пишем программу, которая выведет сумму значений, получившихся после решения выражения 3x-1
<p align="center">![Пишем программу](image/Снимок экрана от 2023-12-02 16-55-16.png){#fig:001 width=70%}</p>
Транслируем файл и смотрим на работу программы
<p align="center">![Проверка](image/Снимок экрана от 2023-12-02 16-55-38.png){#fig:001 width=70%}</p>
# Выводы

Мы научились решать программы с использованием циклов и обработкой аргументов командной строки.

