---

## Front matter

title: "Лабораторная работа № 3. Markdown"

subtitle: "Простейший вариант"

author: "Гусейнов Георгий Русланович"



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

Научиться оформлять отчёты с помощью легковесного языка разметки Markdown.

# Задание
- Сделайте отчёт по предыдущей лабораторной работе в формате Markdown. 
-  В качестве отчёта просьба предоставить отчёты в 3 форматах: pdf, docx и md


# Выполнение лабораторной работы


### Установил git

-   Установим _git_:
    
    ```
    dnf install git
    ```
    

### Установил gh

-   Fedora:
    
    ```
    dnf install gh
    ```
    

## Установил базовае настройка git
-   Зададал имя и email  репозитория:
    
    ```
    git config --global user.name "Name Surname"
    git config --global user.email "work@mail"
    ```
    
-   Настроил utf-8 в выводе сообщений git:
    
    ```
    git config --global core.quotepath false
    ```
-   Настроил верификацию и подписание коммитов git.
-   Зададал имя начальной ветки (будем называть её `master`):
    
    ```
    git config --global init.defaultBranch master
    ```
    
-   Параметр `autocrlf`:
    
    ```
    git config --global core.autocrlf input
    ```
    
-   Параметр `safecrlf`:
    
    ```
    git config --global core.safecrlf warn
    ```
## Создал ключи _pgp_

-   Сгенерировал ключь
    
    ```
    gpg --full-generate-key
    ```
    
-   Из предложенных опций выбирал:
    -   тип _RSA and RSA_;
    -   размер 4096;
    -   выбрал срок действия; значение по умолчанию — 0 (срок действия не истекает никогда).
-   GPG запросит личную информацию, которая сохранится в ключе:
- Ввел:
    -   Имя (не менее 5 символов).
    -   Адрес электронной почты.
        -   При вводе email убедитесь, что он соответствует адресу, используемому на GitHub.
    -   Комментарий. Можно ввести что угодно или нажать клавишу ввода, чтобы оставить это поле пустым.
## Настроил github
## Добавил PGP ключь в GitHub

-   Выводим список ключей и копируем отпечаток приватного ключа:
    
    ```
    gpg --list-secret-keys --keyid-format LONG
    ```
    
-   Отпечаток ключа — это последовательность байтов, используемая для идентификации более длинного, по сравнению с самим отпечатком ключа.
-   Формат строки:
    
    ```
    sec   Алгоритм/Отпечаток_ключа Дата_создания [Флаги] [Годен_до]
          ID_ключа
    ```
    
-   Cкопировал  сгенерированный PGP ключ в буфер обмена:
    
    ```
    gpg --armor --export <PGP Fingerprint> | xclip -sel clip
    ```
    
-   Перешел в настройки GitHub ([https://github.com/settings/keys](https://github.com/settings/keys)), нажал на кнопку _New GPG key_ и вставил полученный ключ в поле ввода.

## Настройка автоматических подписей коммитов git

-   Используя введёный email, указал Git применять его при подписи коммитов:
    
    ```
    git config --global user.signingkey <PGP Fingerprint>
    git config --global commit.gpgsign true
    git config --global gpg.program $(which gpg2)
    ```
## Настройка gh

-   Для начала необходимо авторизоваться
    
    ```
    gh auth login
    ```
    
-   Утилита задаст несколько наводящих вопросов.
-   Авторизоваться можно через броузер.
# Выводы

Научился настраивать и работать с git.
