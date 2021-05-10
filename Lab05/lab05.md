---
# Front matter
lang: ru-RU
title: "Отчет по второй лабораторной работе №5"

author: "Тулеева Валерия, НБИбд-01-20"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
header-includes:
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
---
РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ

Факультет физико-математических и естественных наук
Кафедра прикладной информатики и теории вероятностей







***Основы интерфейса взаимодействия пользователя с системой Unix на уровне командной строки***

**Оглавление:**

1.	Введение:
  a) Цель работы
2.	Описание результатов выполнения задания;
3.	Вывод;
4.	Контрольные вопросы.

























**Введение:**


В операционной системе типа Linux взаимодействие пользователя с системой обычно осуществляется с помощью командной строки посредством построчного ввода команд. При этом обычно используется командные интерпретаторы языка ```shell```: ```/bin/sh```; ```/bin/csh```; ```/bin/ksh```.


*Команда man*. Команда man используется для просмотра (оперативная помощь) в диалоговом режиме руководства (manual) по основным командам операционной системы типа Linux.

*Команда cd*. Команда cd используется для перемещения по файловой системе операционной системы типа Linux.

*Команда pwd*. Для определения абсолютного пути к текущему каталогу исполь- зуется команда pwd (print working directory).

*Команда ls*. Команда ls используется для просмотра содержимого каталога.

*Команда mkdir*. Команда mkdir используется для создания каталогов.

*Команда rm*. Команда rm используется для удаления файлов и/или каталогов.

*Команда history*. Для вывода на экран списка ранее выполненных команд исполь- зуется команда history. Выводимые на экран команды в списке нумеруются. К любой команде из выведенного на экран списка можно обратиться по её номеру в списке, воспользовавшись конструкцией !<номер_команды>.

*Использование символа «;»*. Если требуется выполнить последовательно несколько команд, записанный в одной строке, то для этого используется символ точка с запятой



**Цель работы:**


Приобретение практических навыков взаимодействия пользователя с системой посредством командной строки.


**Описание результатов выполнения задания:**

1. Определила полное имя моего домашнего каталога *(рис 1.1)*:

```ls```

   ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/1:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117697142-f3265400-b1e3-11eb-8ddf-f139da227ab8.png))
   
*Рис 1.1. Определение имени моего домашнего каталога*

2.	Перешла в каталог ```/tmp``` *(рис 2.1)*:

```cd /tmp```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/2:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117697045-d8ec7600-b1e3-11eb-9d17-3ab870d64435.png))
 
*Рис 2.1. Переход в каталог ```/tmp```*

3.	Вывела на экран содержимое каталога ```/tmp```: *(рис 3.1)*

Команда ```ls``` используется для просмотра содержимого каталога.

    ```ls```

Использовала команду ls с различными опциями.

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/3:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117702589-8498c480-b1ea-11eb-8072-e79fe943a808.png))
 
*Рис 3.1. Cодержимое каталога ```/tmp```*

Некоторые файлы в операционной системе скрыты от просмотра и обычно используются для настройки рабочей среды. Имена таких файлов начинаются с точки. Для того, чтобы отобразить имена скрытых файлов, необходимо использовать команду ```ls``` с опцией ```a```:

```ls -a``` *(рис 3.2 и рис 3.3)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/4:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117697299-210b9880-b1e4-11eb-9ab5-9cabfd233eb4.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/5:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117697585-70ea5f80-b1e4-11eb-9a15-9989d670dfdd.png))
 
*Рис 3.2 и рис 3.3. Скрытые файлы каталога*

Чтобы вывести на экран подробную информацию о файлах и каталогах, необходимо использовать опцию ```l```. При этом о каждом файле и каталоге будет выведена следующая информация:
– тип файла,
– право доступа,
– число ссылок,
– владелец,
– размер,
– дата последней ревизии, 
– имя файла или каталога.

```ls -l``` *(рис 3.4 и рис 3.5)*

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/6:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117697655-865f8980-b1e4-11eb-9e40-804e7770821b.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/7:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117697837-c45cad80-b1e4-11eb-8eab-8ea8760d48ac.png))
 
 *Рис 3.4 рис 3.5. Подробная информация*
 
 
4.	Определила ,есть ли в каталоге ```/var/spool``` подкаталог с именем ```cron``` *(рис 4.1)*: 

``` cd /var/spool```

```ls```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/8:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117697980-f4a44c00-b1e4-11eb-9658-312a67bf6998.png))

*Рис 4.1. Подкаталог ```cron```*

5.	Перешла в мой домашний каталог и вывела на экран его содержимое: *(рис 5.1)*

```cd /home``` и ```ls```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/9:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117698070-18679200-b1e5-11eb-916c-02ed3f8ae74b.png))
 
*Рис 5.1. Перешла в ```/home``` и вывела содержимое*

Определила, кто является владельцем файлов и подкаталогов *(рис 5.2)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/10:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117698138-3208d980-b1e5-11eb-83a7-0b3fd18b5a9c.png))

*Рис 5.2. Определила кто владелец*

6.	В домашнем каталоге создала новый каталог с именем ```newdir```: *(рис 6.1)*

```sudo mkdir newdir```

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/11:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117698193-42b94f80-b1e5-11eb-8d84-da1e82cdf6c7.png))
 
*Рис 6.1. Создание нового каталога*

7.	В каталоге ```~/newdir``` создайте новый каталог с именем ```morefun```: *(рис 7.1)*

```cd newdir```;

```sudo mkdir morefun```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/12:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117698226-4ea51180-b1e5-11eb-93bd-864ac7677e7b.png))
 
*Рис 7.1. Создание нового каталога*

8.	В домашнем каталоге создала одной командой три новых каталога с именами letters, memos, misk. Затем удалила эти каталоги одной командой.: *(рис 8.1 и рис 8.2)*

```sudo mkdir letters memos misk```

```sudo rm -r letters memos misk```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/13:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117698265-5b296a00-b1e5-11eb-9106-31875bce4539.png))
 
*Рис 8.1. Создала три каталога*

```sudo rm -r letters memos misk```


![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/14:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117698459-9330ad00-b1e5-11eb-9e48-a684e2b50ec4.png))

*Рис 8.2. Удалила три каталога*


9.  Удалила ранее созданный каталог ```~/newdir``` командой ```rm```. Проверила, был ли каталог удалён.: *(рис 9.1)*

```sudo rm -r newdir```

```ls```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/15:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117698593-b52a2f80-b1e5-11eb-98d6-54979e7e6a56.png))
 
*Рис 9.1. Удалила каталог и проверила, был ли он удален*
 

10.	 С помощью командыman определила, какую опцию команды ```ls``` нужно использовать для просмотра содержимого не только указанного каталога, но и подката-
логов, входящих в него *(рис 10.1 и 10.2)*: 

```man ls```;

``` ls -a``` *(рис 10.3)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/16:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117698676-c7a46900-b1e5-11eb-9e8a-7b0628387d7a.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/17:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117698779-e30f7400-b1e5-11eb-9f85-748da590db66.png))

*Рис 10.1 и 10.2. Команда man ls*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/18:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117699060-341f6800-b1e6-11eb-9586-f93f8439caa7.png))

*Рис 10.3. Команда ld s -a*


11.	С помощью команды ```man``` определила набор опций команды ```ls```, позволяющий отсортировать по времени последнего изменения выводимый список содержимого
каталога с развёрнутым описанием файлов *(рис 11.1 и рис 11.2)*: 

```man ls```;

```ls -alF``` *(рис 11.3)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/16:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117698676-c7a46900-b1e5-11eb-9e8a-7b0628387d7a.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/17:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117698779-e30f7400-b1e5-11eb-9f85-748da590db66.png))

*Рис 11.1 и 11.2. Команда man ls*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/19:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117699238-66c96080-b1e6-11eb-8424-6377266781c0.png))

*Рис 11.3. Команда ls -alF*

12.	 Используя команду ```man``` для просмотра описания следующих команд: ```cd```, ```pwd```, ```mkdir```, ```rmdir```, ```rm```. Пояснила основные опции этих команд: 

 
 ```man cd```; *(рис 12.1)*
 
 Нет справочной страницы для команды cd.
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/cd.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117700173-7d23ec00-b1e7-11eb-8c5e-f6955211fdb1.png))
 
 *Рис 12.1. Команда man cd*
 
 
 ```man pwd```; *(рис 12.2 и рис 12.3)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/20:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117700371-bb211000-b1e7-11eb-985a-bdf970fa75f1.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/21:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117699852-1bfc1880-b1e7-11eb-9b6a-e50dfb9c9782.png))
 
 *Рис 12.4 и 12.5. Команда man pwd*
 
 
 ```man mkdir```; *(рис 12.6 и рис 12.7)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/22:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117700460-ddb32900-b1e7-11eb-844f-92806e6aa163.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/mkdir.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117701671-56ff4b80-b1e9-11eb-9b9e-dce19e159e68.png))
 
 *Рис 12.6 и 12.7. Команда man mkdir*
 
 
 ```man rmdir```; *(рис 12.8 и рис 12.9 )*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/rmdir.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117701710-62527700-b1e9-11eb-8eac-5a620a592dd5.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/28:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117700963-7f3a7a80-b1e8-11eb-9cb7-600b1cb86e89.png))
 
 *Рис 12.8 и 12.9. Команда man rmdir*
 
 
 ```man rm```; *(рис 12.10 и 12.11)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/23:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117700501-ea378180-b1e7-11eb-93ef-8b140c0cfcb5.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/24:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117700562-00454200-b1e8-11eb-9f26-eac9eebfb52b.png))
 
 *Рис 12.10 и 12.11. Команда man rm*


13.	Используя информацию, полученную при помощи команды history, выполнила модификацию и исполнение нескольких команд из буфера команд: *(рис 13.1 и рис 13.2, рис 13.3, рис 13.4)*
 
 ```history```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/25:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117700757-40a4c000-b1e8-11eb-95d7-8f095916f8ea.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/29:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117701052-99745880-b1e8-11eb-82b0-9d6de9ff9480.png))
 
*Рис 13.1 и 13.2. История*


**Модификация**

```!1385:s/alF/F```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/30:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117701314-e6582f00-b1e8-11eb-9997-955e4d1ad94d.png))

*Рис 13.3. Модификация*


**Исполнение нескольких команд из буфера команд**

```cd; ls; pwd```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab05/Screenshot/26:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117700818-54e8bd00-b1e8-11eb-8588-0e0517d8e22d.png))

*Рис 13.4. Исполнение нескольких команд из буфера команд*



**Вывод:**

В данной лабораторной работе, я приобрела практические навыки взаимодействия пользователя с системой посредством командной строки.






