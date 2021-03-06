---
## Front matter
lang: ru-RU
title: Лабораторная работа №7
author: Тимур Андреевич Дарижапов
institute: |
	\inst{1}Российский университет дружбы народов, Москва
	
date: 2021 Москва

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---

# Выполнение лабораторной работы

## 
Цель работы: Ознакомление с инструментами поиска файлов и фильтрации текстовых данных. Приобретение практических навыков: по управлению процессами (и заданиями), по проверке использования диска и обслуживанию файловых систем.

Ход работы :
1.Осуществляю вход в систему, используя своё имя пользователя - tadarizhapov.

##

2.Записываем в файл file.txt названия файлов, содержащихся в каталоге /etc. Дописываем в этот же файл названия файлов, содержащихся в моём домашнем каталоге. Используем команды ls -a /etc > file.txt , ls -a ~ >> file.txt. С помощью команды cat просматриваем содержимое file.txt(Рисунок 1,2).
![Рисунок 1](image/300.png){ width=100% }

##
![Рисунок 2](image/301.png){ width=70% }

##
3.Выводим имена всех файлов из file.txt, имеющих расширение .conf, после чего запишем их в новый текстовой файл conf.txt. Команда grep -e '\.conf$' file.txt > conf.txt.Команда cat conf.txt выводит содержимое conf.txt(Рисунок 3).
![Рисунок 3](image/302.png){ width=100% }

##
4.Определим, какие файлы в нашем домашнем каталоге имеют имена, начинав-шиеся с символа c. Это можно сделать тремя разными способами: find ~ -maxdepth 1 -name "c*" -print, ls ~/c*, ls -a ~ | grep c*(Рисунок 4).
![Рисунок 4](image/303.png){ width=100% }

##
5.Выведем на экран(постранично) имена файлов из каталога /etc, начинающи-еся с символа h(Рисунок 5).
![Рисунок 5](image/304.png){ width=100% }
![Рисунок 6](image/305.png){ width=70% }

##
6.Запустим в фоновом режиме процесс, который будет записывать в файл ~/logfile файлы, имена которых начинаются с log.Команда find / -name "log*" > logfile &(Рисунок 7).Выведем содержимое logfile командой cat logfile.
![Рисунок 7](image/306.png){ width=100% }

##
![Рисунок 8](image/307.png){ width=100% }

##
7.Удалим файл ~/logfile(Рисунок 9).
![Рисунок 9](image/308.png){ width=100% }
8.Запускаем редактор gedit в фоновом режиме командой gedit &(Рисунок 10).
![Рисунок 10](image/309.png){ width=100% }

##
9.Для определения идентификатора процесса gedit, используем команду ps | grep -i "gedit".Наш процесс имеет PID 8559.Идентификатор можно узнать с помощью команд: pgrep gedit и pidof gedit(Рисунок 11).
![Рисунок 11](image/311.png){ width=100% }

##
10.С помощью man узнаём информацию о команде kill.Использую её для завершения процесса(Рисунок 12, 13).
![Рисунок 12](image/312.png){ width=100% }
![Рисунок 13](image/313.png){ width=100% }

##
11.Выполним команды df и du, предварительно прочитав информацию о них с помощью man.
df - утилита, показывающая список всех файловых систем по именам устройств, сообщает их размер, занятое и свободное пространство и точки монтирования.
du - утилита, предназначенная для вывода информации об объёме дискового пространства, занятого файлами и директориями.

##
![Рисунок 14](image/314.png){ width=100% }
![Рисунок 15](image/315.png){ width=100% }

##

![Рисунок 16](image/316.png){ width=100% }
![Рисунок 17](image/317.png){ width=100% }

##
![Рисунок 18](image/318.png){ width=100% }

##
12.Выведем имена всех директорий,имеющихся в нашем домашнем каталоге с помощью find ~ -type d, предварительно написав man find.
![Рисунок 19](image/319.png){ width=100% }

##
Вывод: Я ознакомился с инструментами поиска файлов и фильтрации текстовых данных и приобрёл практические навыки по управлению процессами (и заданиями), по проверке использования диска и обслуживанию файловых систем.

