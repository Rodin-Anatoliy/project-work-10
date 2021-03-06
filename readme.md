# Форма для регитсрации
Валидация полей через регулярные выражения, работа с Git и Github
#
[Ссылка на рабочую версию проекта](https://rodin-anatoliy.github.io/project-work-10/)

Версия проекта v0.8 - fixed 2.0

Дизайн и визуальное оформление предоставлены [Яндекс.Практикум](https://praktikum.yandex.ru/)


## В проекте реализовано:

**1 Git и «командная строка»:**

- Создание репозитория на сайте github.
- Командами в терминале скопировать репозиторий на компьютер.
- В папку репозитория поместить файлы: https://code.s3.yandex.net/web-developer/project-10/validation.zip.
- Создать и оформить файл readme.md. В заголовок вынесити ссылку на рабочую версию формы. Указать в файле версию проекта.
- Прописывать версию после каждого коммита.


**2 Регулярные выражения, валидация полей:**

- *Поле "Name":*
    - только кириллица;
    - первая буква заглавная;
    - можно ввести от 2 до 20 символов — это можно задать в атрибутах minlength и maxlength;
    - возможна запись двойных имён — например, Анна-Мария;
    - шаблон должен находить имена таких форматов:
        - Ян
        - Максим
        - Серёга
        - Ёль
        - Джон-Дон

- *Поле "Email":*
    - только латиница;
    - «собака» @ — обязательный символ;
    - точка . — тоже обязательный символ;
    - цифры, подчерк, тире — разрешённые символы;
    - шаблон должен находить e-mail таких форматов:
        - ya2@2ya.ru - имя и домен могут содержать цифры
        - ya-e@ya-ya.ru - имя и домен могут содержать тире
        - ya@x.ru - доменное имя может состоять из одного символа
        - y@ya.ru - имя ящика может состоять из одного символа
        - some@mail.ya.ru - доменное имя может содержать поддомен

- *Поле "Телефон":*
    - шаблон для телефона должен находить номера таких форматов:
        - +7(925)900-90-90
        - +7(925) 900-90-90
        - +7 925-900-90-90
        - +79259009090
        - 89259009090

- *Поле "Сайт":*
    - начинается с http:// или https://;
    - затем www. — это необязательная группа;
    - IP-адрес — 255.255.255.255 или доменное имя — stasbasov.ru;
    - порт — тоже необязательная группа. Порт начинается с двоеточия, за которым идут от 2 до 5 цифр. Например: :8080;
    - путь — последовательность из цифр, слешей и латинских букв, на конце которого может стоять решётка #;
    - шаблон должен находить url таких форматов:
        - http://ya.ru
        - https://www.ya.ru
        - http://2-domains.ru
        - http://ya.ru:98/
        - http://ya.com:30
        - http://ya.ru/path/to/deep/
        - http://ya-ya-ya.ru
        - http://8.8.8.8:8080
        - http://8.8.8.8:8080/page/to/deep#
