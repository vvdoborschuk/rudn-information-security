---
title: "Упражнение ко второму блоку. Основы моделирования в Xcos"
subtitle: "Моделирование информационных процессов"
institute: "Российский Университет Дружбы Народов"
author: [Доборщук Владимир Владимирович, НФИбд-01-18]
date: "15 мая 2021"
keywords: [Моделирование, Лабораторная]
lang: "ru"
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
fontsize: 12pt
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: Fira Sans
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
titlepage: true
titlepage-text-color: "000000"
titlepage-rule-color: "1A1B35"
titlepage-rule-height: 2
listings-no-page-break: true
indent: true
header-includes:
  - \usepackage{sectsty}
  - \sectionfont{\clearpage}
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
...

# Цели и задачи

**Цель:** Изучить основы работы с Scilab системой компьютерной математики, предназначенная для решения вычислительных задач, а также получить практический опыт с Xcos (модулем для визуального моделирования).

**Задачи:**

Построить с помощью Xcos фигуры Лиссажу со следующими параметрами:

* $A = B = 1, a = 2, b = 2, \delta = 0; \pi/4; \pi/2; 3\pi/4; \pi$;
* $A = B = 1, a = 2, b = 4, \delta = 0; \pi/4; \pi/2; 3\pi/4; \pi$;
* $A = B = 1, a = 2, b = 6, \delta = 0; \pi/4; \pi/2; 3\pi/4; \pi;$
* $A = B = 1, a = 2, b = 3, \delta = 0; \pi/4; \pi/2; 3\pi/4;$

# Ход выполнения лабораторной работы

Исходя из описания лабораторной работы, опустим блок описания построения модели, так как данный процесс был выполнен на записи выполнения.

От нас требуется продемонстрировать изменения фигур Лиссажу в зависимости от изменения параметров $\delta$ и $b$.

## Случай при $A = B = 1, a = 2, b = 2$

Рассмотрим данное состояние для различных $\delta$ (в данном случае у нас идет соотношение $1:1$):

![$b = 2,\delta=0$](image/1_0.png)

![$b = 2,\delta=\pi/4$](image/1_pi4.png)

![$b = 2,\delta=\pi/2$](image/1_pi2.png)

![$b = 2,\delta=3\pi/4$](image/1_3pi4.png)

![$b = 2,\delta=\pi/2$](image/1_pi2.png)

## Случай при $A = B = 1, a = 2, b = 4$

Рассмотрим данное состояние для различных $\delta$ (в данном случае у нас идет соотношение $1:2$):

![$b = 4,\delta=0$](image/2_0.png)

![$b = 4,\delta=\pi/4$](image/2_pi4.png)

![$b = 4,\delta=\pi/2$](image/2_pi2.png)

![$b = 4,\delta=3\pi/4$](image/2_3pi4.png)

![$b = 4,\delta=\pi/2$](image/2_pi2.png)

## Случай при $A = B = 1, a = 2, b = 6$

Рассмотрим данное состояние для различных $\delta$ (в данном случае у нас идет соотношение $1:3$):

![$b = 6,\delta=0$](image/3_0.png)

![$b = 6,\delta=\pi/4$](image/3_pi4.png)

![$b = 6,\delta=\pi/2$](image/3_pi2.png)

![$b = 6,\delta=3\pi/4$](image/3_3pi4.png)

![$b = 6,\delta=\pi/2$](image/3_pi2.png)

## Случай при $A = B = 1, a = 2, b = 3$

Рассмотрим данное состояние для различных $\delta$ (в данном случае у нас идет соотношение $2:3$):

![$b = 3,\delta=0$](image/4_0.png)

![$b = 3,\delta=\pi/4$](image/4_pi4.png)

![$b = 3,\delta=\pi/2$](image/4_pi2.png)

![$b = 3,\delta=3\pi/4$](image/4_3pi4.png)

![$b = 3,\delta=\pi/2$](image/4_pi2.png)

# Анализ результатов

Вид фигур Лиссажу непосредственно зависит от соотношения частот одного генератора к другому ($a:b$), а значение фазового сдвига определяет поворот фигуры.

# Выводы

Мы успешно изучили основы работы с Scilab выполнили все поставленные задачи, тем самым практически закрепили опыт работы в Xcos.