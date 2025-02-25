---
## Front matter
lang: ru-RU
title: Упражнение (xcos)
subtitle: Построение фигур Лиссажу
author:
  - Дворкина Е. В.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 14 февраля 2025

## i18n babel
babel-lang: russian
babel-otherlangs: english

## Formatting pdf
toc: false
toc-title: Содержание
slide_level: 2
aspectratio: 169
section-titles: true
theme: metropolis
header-includes:
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
---

## Докладчик

:::::::::::::: {.columns align=center}
::: {.column width="70%"}

  * Дворкина Ева Владимировна
  * студентка
  * группа НФИбд-01-22
  * Российский университет дружбы народов
  * [1132226447@rudn.ru](mailto:1132226447@rudn.ru)
  * <https://github.com/evdvorkina>

:::
::: {.column width="30%"}

![](./image/я.jpg)

:::
::::::::::::::

## Цель работы

Цель данной лабораторной работы - выполнить упражнение по ознакомлению с инструментом *xcos*

## Задание

Постройте с помощью xcos фигуры Лиссажу со следующими параметрами:

1) $A = B = 1, a = 2, b = 2, \, \delta = 0; \, \pi/4; \, \pi/2; \,  3\pi/4;\,  \pi;$

2) $A = B = 1, a = 2, b = 4, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3\pi/4; \, \pi;$

3) $A = B = 1, a = 2, b = 6, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3π/4; \, π;$

4) $A = B = 1, a = 2, b = 3, \, \delta = 0; \, \pi/4; \, \pi/2; \, 3\pi/4; \, \pi.$


## Математическое выражение для кривой Лиссажу

$$
\begin{cases}
  x(t) = A sin(at + \delta),\\
  y(t) = B sin(bt),
\end{cases}
$$

где $A$, $B$ -- амплитуды колебаний, $a$, $b$ -- частоты, $\delta$ -- сдвиг фаз.

## Блоки xcos

- CLOCK_c -- запуск часов модельного времени;
- GENSIN_f -- блок генератора синусоидального сигнала;
- CANIMXY -- анимированное регистрирующее устройство для построения графика типа y = f(x);
- TEXT_f -- задаёт текст примечаний.

## Модель для построения фигур Лиссажу в xcos

![Модель для построения фигуры Лиссажу в xcos](image/1.PNG){#fig:001 width=70%}

## Настройка параметров генератора синусоидальных колебаний

![Ввод параметров для генератора синусоидальных колебаний](image/3.PNG){#fig:002 width=70%}

## Настройка параметров генератора синусоидальных колебаний

![Ввод параметров для генератора синусоидальных колебаний](image/4.PNG){#fig:0021 width=70%}

## Настройка параметров CANIMXY

![Ввод параметров для CANIMXY](image/2.PNG){#fig:003 width=70%}

## $A = B = 1, a = 2, b = 2, \delta = 0$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = 0$](image/5.PNG){#fig:004 width=70%}

## $A = B = 1, a = 2, b = 2, \delta = \pi/4$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi /4$](image/6.PNG){#fig:005 width=70%}

## $A = B = 1, a = 2, b = 2, \delta = \pi/2$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi /2$](image/7.PNG){#fig:006 width=70%}

## $A = B = 1, a = 2, b = 2, \delta = 3\pi/4$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = 3\pi /4$](image/8.PNG){#fig:007 width=70%}

## $A = B = 1, a = 2, b = 2, \delta = \pi$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 2, \delta = \pi$](image/9.PNG){#fig:008 width=70%}

## Изменение параметров на втором генераторе

![Ввод параметров для генератора синусоидальных колебаний](image/10.PNG){#fig:009 width=70%}

## $A = B = 1, a = 2, b = 4, \delta = 0$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = 0$](image/11.PNG){#fig:010 width=70%}

## $A = B = 1, a = 2, b = 4, \delta = \pi/4$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi /4$](image/12.PNG){#fig:011 width=70%}

## $A = B = 1, a = 2, b = 4, \delta = \pi/2$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi /2$](image/13.PNG){#fig:012 width=70%}

## $A = B = 1, a = 2, b = 4, \delta = 3\pi/4$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = 3\pi /4$](image/14.PNG){#fig:013 width=70%}

## $A = B = 1, a = 2, b = 4, \delta = \pi$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 4, \delta = \pi$](image/15.PNG){#fig:014 width=70%}

## Изменение параметров на втором генераторе 

![Ввод параметров для генератора синусоидальных колебаний](image/16.PNG){#fig:015 width=70%}

## $A = B = 1, a = 2, b = 6, \delta = 0$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = 0$](image/17.PNG){#fig:016 width=70%}

## $A = B = 1, a = 2, b = 6, \delta = \pi/4$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi /4$](image/18.PNG){#fig:017 width=70%}

## $A = B = 1, a = 2, b = 6, \delta = \pi/2$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi /2$](image/19.PNG){#fig:018 width=70%}

## $A = B = 1, a = 2, b = 6, \delta = 3\pi/4$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = 3\pi /4$](image/20.PNG){#fig:019 width=70%}

## $A = B = 1, a = 2, b = 6, \delta = \pi$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 6, \delta = \pi$](image/21.PNG){#fig:020 width=70%}

## Изменение параметров на втором генераторе

![Ввод параметров для генератора синусоидальных колебаний](image/22.PNG){#fig:021 width=70%}

## $A = B = 1, a = 2, b = 3, \delta = 0$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = 0$](image/23.PNG){#fig:022 width=70%}

## $A = B = 1, a = 2, b = 3, \delta = \pi/4$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi /4$](image/24.PNG){#fig:023 width=70%}

## $A = B = 1, a = 2, b = 3, \delta = \pi/2$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi /2$](image/25.PNG){#fig:024 width=70%}

## $A = B = 1, a = 2, b = 3, \delta = 3\pi/4$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = 3\pi /4$](image/26.PNG){#fig:025 width=70%}

## $A = B = 1, a = 2, b = 3, \delta = \pi$

![Фигура Лиссажу: $A = B = 1, a = 2, b = 3, \delta = \pi$](image/27.PNG){#fig:026 width=70%}

## Выводы

В результате выполнения данной лабораторной работы я выполнила упражнение по ознакомлению с программой *xcos*.

# Спасибо за внимание!
