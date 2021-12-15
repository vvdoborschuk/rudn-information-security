---
## Front matter
title: "Лабораторная работа №5: Дискреционное разграничение прав в Linux. Исследование влияния дополнительных атрибутов"
subtitle: "*дисциплина: Информационная безопасность*"
author: "Швец Сергей Сергеевич"
date: 2021, 13 November

## Formatting
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
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


# Цель работы

Изучение механизмов изменения идентификаторов, применения
SetUID- и Sticky-битов. Получение практических навыков работы в консоли с дополнительными атрибутами. Рассмотрение работы механизма
смены идентификатора процессов пользователей, а также влияние бита
Sticky на запись и удаление файлов.

# Выполнение работы

## отключение системы запретов

Так как программы с установленным битом SetUID могут представлять
большую брешь в системе безопасности, в современных системах используются дополнительные механизмы защиты. Чтобы система
защиты SELinux не мешала выполнению заданий работы, она была отключена до следующей перезагрузки.

![отключение системы запретов](10.jpg){ #fig:001 width=70% }

## Создание программы simpleid

Создание программы simpleid.

![Guest](1.jpg){ #fig:002 width=70% }

## компиляция, запуск программы, а также команды id

Далее программа была скомпилирована и запущена, а также было проведено сравнение результатов работы программы с командой id

![директория и пользователь](2.jpg){ #fig:003 width=70% }


## модификация программы


Далее программа была модифицирована несколькими атрибутами.

![модификация программы ](3.jpg){ #fig:005 width=70% }

## пункт 8

Выполнение команд из пункта 8.

![8 пункт](4.jpg){ #fig:006 width=70% }

## программа readfile.c

Написание программы readfile.

![readfile](5.jpg){ #fig:007 width=70% }

## пункты 15-19

Проверка доступа.

![Расширинные атрибуты](6.jpg){ #fig:008 width=70% }

## пункты 1-3 с файлом file01

Создание файла file01.

![file01](7.jpg){ #fig:009 width=70% }


## Guest2

попытка прочитать и изменить файле file01 от имени пользователя, не являющегося владельцем файла

![guest2](8.jpg){ #fig:011 width=70% }

## Модификация атрибутов

модификация атрибутов директории от имени пользователя guest2

![атрибуты](9.jpg){ #fig:012 width=70% }


# Выводы

Мной были изучены механизмы изменения идентификаторов, применение SetUID- и Stickyбиты. Получены практические навыкы работы в консоли с дополнительными
атрибутами. Рассмотрена работа механизмов смены идентификаторов процесса
пользователей, а также влияние бита Sticky на запись и удаление файлов.