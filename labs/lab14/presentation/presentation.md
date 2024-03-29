---
## Front matter
lang: ru-RU
title: Презентация по лабораторной работе №14
subtitle: "Именованные каналы"
author:
  - Гусейнов Георгий, НКАбд-04-22
institute:
  - Российский университет дружбы народов, Москва, Россия
date: 07.05.2023

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
  - '\makeatletter'
  - '\beamer@ignorenonframefalse'
  - '\makeatother'
---

## Цель работы

Приобретение практических навыков работы с именованными каналами.

## Основные задачи

Изучите приведённые в тексте программы server.c и client.c. Взяв данные примеры
за образец, напишите аналогичные программы, внеся следующие изменения:

1. Работает не 1 клиент, а несколько (например, два).
2. Клиенты передают текущее время с некоторой периодичностью (например, раз в пять
   секунд). Используйте функцию sleep() для приостановки работы клиента.
3. Сервер работает не бесконечно, а прекращает работу через некоторое время (напри-
   мер, 30 сек). Используйте функцию clock() для определения времени работы сервера.
   Что будет в случае, если сервер завершит работу, не закрыв канал?

## Процесс выполнения

Изучите приведённые в тексте программы server.c и client.c. Взяв данные примеры за образец, напишите аналогичные программы, внеся следующие изменения:

1. Работает не 1 клиент, а несколько (например, два)
2. Клиенты передают текущее время с некоторой периодичностью (например, раз в пять секунд). Используйте функцию sleep() для приостановки работы клиента.

3. Сервер работает не бесконечно, а прекращает работу через некоторое время (например, 30 сек). Используйте функцию clock() для определения времени работы сервера. Что будет в случае, если сервер завершит работу, не закрыв канал?

В процессе выполнения лабораторной работы я приобрел практические навыки работы с именованными каналами.

# Спасибо за внимание!
