---
## Front matter
title: "Выполнение упражнения (xcos)"
subtitle: "Построение фигур Лиссажу"
author: "Дворкина Ева Владимировна"

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
lot: false # List of tables
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

Цель данной лабораторной работы - выполнить упражнение по ознакомлению с инструментом *xcos*

# Задание

Постройте с помощью xcos фигуры Лиссажу со следующими параметрами:

1) $A = B = 1, a = 2, b = 2, \, \delta = 0; \, \pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$

2) $A = B = 1, a = 2, b = 4, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3\pi/4; \, \pi;$

3) $A = B = 1, a = 2, b = 6, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3π/4; \, π;$

4) $A = B = 1, a = 2, b = 3, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3\pi/4; \, \pi.$

# Теоретические сведения

**Scilab** — система компьютерной математики, предназначенная для решения вычислительных задач [@xcos].

Основное окно Scilab содержит обозреватель файлов, командное окно, обозреватель переменных и журнал команд

Программа xcos является приложением к пакету Scilab. Для вызова окна xcos необходимо в меню основного окна Scilab выбрать Инструменты, Визуальное моделирование xcos.

При моделировании с использованием xcos реализуется принцип визуального программирования, в соответствии с которым пользователь на экране из палитры блоков создаёт модель и осуществляет расчёты.

# Выполнение лабораторной работы

Математическое выражение для кривой Лиссажу:

$$
\begin{cases}
  x(t) = A sin(at + \delta),\\
  y(t) = B sin(bt),
\end{cases}
$$

где $A$, $B$ -- амплитуды колебаний, $a$, $b$ -- частоты, $\delta$ -- сдвиг фаз.

В модели, изображённой на рис. [-@fig:001], использованы следующие блоки xcos:

- CLOCK_c -- запуск часов модельного времени;
- GENSIN_f -- блок генератора синусоидального сигнала;
- CANIMXY -- анимированное регистрирующее устройство для построения графика типа y = f(x);
- TEXT_f -- задаёт текст примечаний.

![Модель для построения фигуры Лиссажу в xcos](image/1.PNG){#fig:001 width=70%}

Щелкнув правой кнопкой мышки по генератору синусоидальный колебаний, откроем вкладку параметры на редактирование и внесем нужные данные (рис. [-@fig:002]). 

![Ввод параметров для генератора синусоидальных колебаний](image/3.PNG){#fig:002 width=70%}

Щелкнув правой кнопкой мышки по второму генератору синусоидальный колебаний, откроем вкладку параметры на редактирование и внесем нужные данные (рис. [-@fig:0021]). 

![Ввод параметров для генератора синусоидальных колебаний](image/4.PNG){#fig:0021 width=70%}

Таким же образом введем параметры в регистрирующее устройство (рис. [-@fig:003]).

![Ввод параметров для CANIMXY](image/2.PNG){#fig:003 width=70%}

Выполнив моделирование получим следующий график фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 2, \delta = 0$ (рис. [-@fig:004]). Меняя фазу в первом генераторе на $\pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$ соответственно получим другие фигуры Лиссажу (рис. [-@fig:005]-[-@fig:008]).

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = 0$](image/5.PNG){#fig:004 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi /4$](image/6.PNG){#fig:005 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi /2$](image/7.PNG){#fig:006 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = 3\pi /4$](image/8.PNG){#fig:007 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi$](image/9.PNG){#fig:008 width=70%}

Изменим параметр частоты на втором генераторе (рис. [-@fig:009]).

![Ввод параметров для генератора синусоидальных колебаний](image/10.PNG){#fig:009 width=70%}

Выполнив моделирование получим следующий график фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 4, \delta = 0$ (рис. [-@fig:010]). Меняя фазу в первом генераторе на $\pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$ соответственно получим другие фигуры Лиссажу (рис. [-@fig:011]-[-@fig:014]).

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = 0$](image/11.PNG){#fig:010 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi /4$](image/12.PNG){#fig:011 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi /2$](image/13.PNG){#fig:012 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = 3\pi /4$](image/14.PNG){#fig:013 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi$](image/15.PNG){#fig:014 width=70%}

Изменим параметр частоты на втором генераторе (рис. [-@fig:015]).

![Ввод параметров для генератора синусоидальных колебаний](image/16.PNG){#fig:015 width=70%}

Выполнив моделирование получим следующий график фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 6, \delta = 0$ (рис. [-@fig:016]). Меняя фазу в первом генераторе на $\pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$ соответственно получим другие фигуры Лиссажу (рис. [-@fig:017]-[-@fig:020]).

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = 0$](image/17.PNG){#fig:016 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi /4$](image/18.PNG){#fig:017 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi /2$](image/19.PNG){#fig:018 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = 3\pi /4$](image/20.PNG){#fig:019 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi$](image/21.PNG){#fig:020 width=70%}

Изменим параметр частоты на втором генераторе (рис. [-@fig:021]).

![Ввод параметров для генератора синусоидальных колебаний](image/22.PNG){#fig:021 width=70%}

Выполнив моделирование получим следующий график фигуры Лиссажу при параметрах: $A = B = 1, a = 2, b = 4, \delta = 0$ (рис. [-@fig:022]). Меняя фазу в первом генераторе на $\pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$ соответственно получим другие фигуры Лиссажу (рис. [-@fig:023]-[-@fig:026]).

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = 0$](image/23.PNG){#fig:022 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi /4$](image/24.PNG){#fig:023 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi /2$](image/25.PNG){#fig:024 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = 3\pi /4$](image/26.PNG){#fig:025 width=70%}

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi$](image/27.PNG){#fig:026 width=70%}

# Выводы

В результате выполнения данной лабораторной работы я выполнила упражнение по ознакомлению с программой *xcos*.

# Список литературы{.unnumbered}

::: {#refs}
:::
