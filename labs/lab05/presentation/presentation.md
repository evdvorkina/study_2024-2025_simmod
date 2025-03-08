---
## Front matter
lang: ru-RU
title: Лабораторная работа №5
subtitle: Модель эпидемии (SIR)
author:
  - Дворкина Е. В.
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 8 марта 2025

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

Исследование модели эпидемии (SIR) с помощью xcos и OpenModelica.

## Задание

- Реализовать классическую модель SIR с помощью xcos(в том числе с помощью блока Modelica) и OpenModelica.
- Реализовать модель SIR с учетом демографических признаков с помощью xcos(в том числе с помощью блока Modelica) и OpenModelica.
- Исследовать модель SIR с учетом демографических признаков, изменяя параметры.

## Теоретическое введение

$$
\begin{cases}
	\frac{dS}{dt} = - \frac{\beta I S}{N}, \\
	\frac{dI}{dt} = \frac{\beta I S}{N} - \nu I, \\
	\frac{dR}{dt} = \nu I,
\end{cases}
$$

# Выполнение лабораторной работы

## Задать контекст в xcos

![Задать контекст в xcos](image/1.PNG){#fig:001 width=70%}

## Реализация модели в xcos

![Модель SIR в xcos](image/4.PNG){#fig:004 width=70%}

## Начальные значения интегрирования

![Задать начальное значение в блоке интегрирования](image/5.PNG){#fig:005 width=70%}

## Время моделирования

![Задать конечное время интегрирования в xcos](image/7.PNG){#fig:007 width=70%}

## Параметры регистрирующего устрйоства

![Задать значения отображения графиков в регистрирующем устройстве](image/8.PNG){#fig:008 width=70%}

## Решение модели

![График решения модели SIR при $\beta = 1$, $\nu = 0.3$](image/9.PNG){#fig:009 width=70%}

## Реализация модели с помощью блока Modelica (настройка блока)

![Настройка параметров блока Modelica](image/10.PNG){#fig:010 width=70%}

## Реализация модели с помощью блока Modelica (настройка блока)

![Настройка параметров блока Modelica](image/11.PNG){#fig:011 width=70%}

## Реализация модели с помощью блока Modelica в xcos

![Модель SIR в xcos с применением блока Modelica](image/12.PNG){#fig:012 width=70%}

## Решение модели

![График решения модели SIR при $\beta = 1$, $\nu = 0.3$](image/13.PNG){#fig:013 width=70%}

## Реализация модели в OpenModelica

![Модель в OpenModelica](image/14.PNG){#fig:014 width=70%}

## Решение модели

![График решения модели SIR при $\beta = 1$, $\nu = 0.3$](image/15.PNG){#fig:015 width=70%}

# Задание для самостоятельного выполнения

## Модель SIR с учетом демографии

$$
\begin{cases}
\frac{dS}{dt} = - \beta I S + \mu (N - S), \\
\frac{dI}{dt} = \beta I S - \nu I - \mu I, \\
\frac{dR}{dt} = \nu I - \mu R,
\end{cases}
$$

## Задать переменные окружения

![Задать переменные окружения в xcos](image/17.PNG){#fig:016 width=70%}

## Реализация модели в xcos

![Модель SIR с учетом демографии в xcos](image/16.PNG){#fig:017 width=70%}


## Решение модели с параметрами $\beta = 1$, $\nu = 0.3$, $\mu = 0.1$

![График решения модели SIR с учетом демографии при $\beta = 1$, $\nu = 0.3$, $\mu = 0.1$](image/18.PNG){#fig:018 width=70%}

## Реализация модели с помощью блока Modelica в xcos (настройка блока)

![Настройка параметров блока Modelica](image/19.PNG){#fig:019 width=70%}

## Реализация модели с помощью блока Modelica в xcos (настройка блока)

![Настройка параметров блока Modelica](image/20.PNG){#fig:020 width=70%}

## Реализация модели с помощью блока Modelica в xcos

![Модель SIR в xcos с применением блока Modelica](image/21.PNG){#fig:021 width=70%}

## Решение модели с параметрами $\beta = 1$, $\nu = 0.3$, $\mu = 0.1$

![График решения модели SIR с учетом демографии при $\beta = 1$, $\nu = 0.3$, $\mu = 0.1$](image/22.PNG){#fig:022 width=70%}

## Реализация модели в OpenModelica

![Модель SIR с учетом демографии в OpenModelica](image/23.PNG){#fig:023 width=70%}

## Задать параметры моделирования

![Параметры моделирования в OpenModelica](image/24.PNG){#fig:024 width=70%}

## Решение модели с параметрами $\beta = 1$, $\nu = 0.3$, $\mu = 0.1$

![График решения модели SIR с учетом демографии при $\beta = 1$, $\nu = 0.3$, $\mu = 0.1$](image/25.PNG){#fig:025 width=70%}

# Анализ графиков при разных параметрах модели


## Решение модели с параметрами $\beta = 1$, $\nu = 0.3$, $\mu = 0.3$

![График решения модели SIR с учетом демографии при $\beta = 1$, $\nu = 0.3$, $\mu = 0.3$. OpenModelica](image/26.PNG){#fig:026 width=70%}

## Решение модели с параметрами $\beta = 1$, $\nu = 0.3$, $\mu = 0.5$

![График решения модели SIR с учетом демографии при $\beta = 1$, $\nu = 0.3$, $\mu = 0.5$. OpenModelica](image/27.PNG){#fig:027 width=70%}

## Решение модели с параметрами $\beta = 1$, $\nu = 0.3$, $\mu = 0.05$

![График решения модели SIR с учетом демографии при $\beta = 1$, $\nu = 0.3$, $\mu = 0.05$. OpenModelica](image/28.PNG){#fig:028 width=70%}

## Решение модели с параметрами $\beta = 1.5$, $\nu = 0.2$, $\mu = 0.2$
![График решения модели SIR с учетом демографии при $\beta = 1.5$, $\nu = 0.2$, $\mu = 0.2$. OpenModelica](image/29.PNG){#fig:029 width=70%}

## Решение модели с параметрами $\beta = 1$, $\nu = 0.5$, $\mu = 0.2$

![График решения модели SIR с учетом демографии при $\beta = 1$, $\nu = 0.5$, $\mu = 0.2$. OpenModelica](image/30.PNG){#fig:030 width=70%}

## Выводы

В результате выполнения работы была исследована модель SIR при помощи xcos и OpenModelica.

