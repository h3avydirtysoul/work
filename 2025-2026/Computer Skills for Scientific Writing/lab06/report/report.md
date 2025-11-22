---
## Front matter
title: "Отчет по лабораторной работе №6"
subtitle: "Дисциплина: Computer Skills for Scientific Writing "
author: "Дарижапов Тимур Андреевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl
link-citations: true

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt

## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
## Критически важные настройки для русского языка
mainfont: IBM Plex Serif
## I18n polyglossia
## Настройки для русского языка
polyglossia-lang:
  name: russian
  options:
    - spelling=modern
    - babelshorthands=true
polyglossia-otherlangs:
  name: english

romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
# lofTitle: "Список иллюстраций"
# lotTitle: "Список таблиц"
# lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

### **Лабораторная работа № 6. Библиография в LaTeX**

### **Цель работы**

Научиться работать с системой библиографических ссылок BibTeX и BibLaTeX и оформлять цитирования в соответствии с требованиями научных публикаций.

## **Ход работы**

### **1. Создание файла .tex**

![](image/1.jpg)


### **2. Создание файла .bib**


![](image/2.jpg)

Во второй колонке задан параметр `p{9cm}`. Это позволяет ограничить ширину ячейки и автоматически переносить строки при необходимости.

### **3. Компиляция**

Компиляция файла с библиографией происходит с помощью комбинации следующих команд:

```
pdflatex sixth.tex
bibtex sixth.aux
pdflatex sixth.tex
pdflatex sixth.tex
```
Я назвал файлы именем sixth.tex и sixth.bib. Команда bibtex sixth.aux ищет файл sixth.bib для оформления библиографии.

![](image/3.jpg)


### **Вывод**

Я научился работать с системой библиографических ссылок BibTeX и BibLaTeX и оформлять цитирования в соответствии с требованиями научных публикаций.


