---
## Front matter
title: "отчет по лабораторной работе N1"
subtitle: "операционные системы"
author: "Гусейнов ГР"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output formaSSSt
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
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

-   Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов.


# Задание
### Запуск приложения для установки системы

-   Загрузите LiveCD.
-   Появится интерфейс начальной конфигурации.
-   Нажмите _Enter_ для создания конфигурации по умолчанию.
-   Нажмите _Enter_, чтобы выбрать в качестве модификатора клавишу _Win_ (она же клавиша _Super_).
-   В файле конфигурации эта клавиша будет обозначена как `$Mod`.
-   Нажмите комбинацию _Win+Enter_ для запуска терминала.
-   В терминале запустите `liveinst`.
-   Для перехода к раскладке окон с табами нажмите _Win+w_.

### Установка системы на диск

![pictutre](image/placeimg_800_600_tech.jpg)

-   Выберите язык интерфейса и перейдите к настройкам установки операционной системы.
-   При необходимости скорректируйте часовой пояс, раскладку клавиатуры (рекомендуется в качестве языка по умолчанию указать английский язык).
-   Место установки ОС оставьте без изменения.
-   Установите имя и пароль для пользователя `root`.
-   Установите имя и пароль для Вашего пользователя.
-   Задайте сетевое имя Вашего компьютера.
-   После завершения установки операционной системы корректно перезапустите виртуальную машину.
-   В VirtualBox оптический диск должен отключиться автоматически, но если это не произошло, то необходимо отключить носитель информации с образом.

# Домашнее задание

-   Дождитесь загрузки графического окружения и откройте терминал. В окне терминала проанализируйте последовательность загрузки системы, выполнив команду `dmesg`. Можно просто просмотреть вывод этой команды:

    
    dmesg | less

    
-   Можно использовать поиск с помощью `grep`:
    
    
    dmesg | grep -i "то, что ищем"


-   Получите следующую информацию.
    -   Версия ядра Linux (Linux version).
    -   Частота процессора (Detected Mhz processor).
    -   Модель процессора (CPU0).
    -   Объём доступной оперативной памяти (Memory available).
    -   Тип обнаруженного гипервизора (Hypervisor detected).
    -   Тип файловой системы корневого раздела.
    -   Последовательность монтирования файловых систем.



# Выполнение лабораторной работы

Описываются проведённые действия, в качестве иллюстрации даётся ссылка на иллюстрацию (рис. @fig:001).

# Выводы

Вывод я научился устанавливать операционные системына VBox.

# Контрольные вопросы

1.  Какую информацию содержит учётная запись пользователя?
    
2.  Укажите команды терминала и приведите примеры:
    
    -   для получения справки по команде;  <команда> --help
    -   для перемещения по файловой системе; cd <дериктория>
    -   для просмотра содержимого каталога; ls <дериктория>
    -   для определения объёма каталога; pwd
    -   для создания / удаления каталогов / файлов; mkdir  <имя каталога>/ rm <имя каталога> / touch <имя файла. + расширение>
    -   для задания определённых прав на файл / каталог;   chmod <разрешение> <путь/имя каталога>
    -   для просмотра истории команд.  history
3.  Что такое файловая система? Приведите примеры с краткой характеристикой.
    Файловая система – это инструмент, позволяющий операционной системе и программам обращаться к нужным файлам и работать с ними.
	FAT32
1.  Как посмотреть, какие файловые системы подмонтированы в ОС? findmnt
2.  Как удалить зависший процесс? kill <имя процесора>
