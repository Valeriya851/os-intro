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



   ![]()
   
*Рис 1.1. Определение имени моего домашнего каталога*

2.	Перешла в каталог ```/tmp``` *(рис 2.1)*:

```cd /tmp```
 
 ![]()
 
*Рис 2.1. Переход в каталог ```/tmp```*

3.	Вывела на экран содержимое каталога ```/tmp```: *(рис 3.1)*

    ```ls```

Использовала команду ls с различными опциями.

![]()
 
*Рис 3.1. Cодержимое каталога ```/tmp```*
 
 **Разница в выводимой на экран информации.**
 
 *(рис 3.1, рис 3.2, рис 3.3 и рис 3.4)*
 
 ![]()
 
*Рис 3.2. *

 ![]()
 
 *Рис 3.3. *
 
 ![]()
 
 *Рис 3.4. *
 
4.	Определила ,есть ли в каталоге ```/var/spool``` подкаталог с именем ```cron``` *(рис 4.1)*: 

```ls```

![]()

*Рис 4.1. Подкаталог ```cron```*

5.	Перешла в мой домашний каталог и вывела на экран его содержимое: *(рис 5.1)*

```cd /home``` и ```ls```
 
 ![]()
 
*Рис 5.1. Перешла в ```/home``` и вывела содержимое*

Определила, кто является владельцем файлов и подкаталогов *(рис 5.2)*:


![]()

*Рис 5.2. Определила кто владелец*

6.	В домашнем каталоге создала новый каталог с именем ```newdir```: *(рис 6.1)*

```sudo mkdir newdir```

 
 ![]()
 
*Рис 6.1. Создание нового каталога*

7.	В каталоге ```~/newdir``` создайте новый каталог с именем ```morefun```: *(рис 7.1)*

```cd newdir```;

```sudo mkdir morefun```
 
 ![]()
 
*Рис 7.1. Создание нового каталога*

8.	В домашнем каталоге создала одной командой три новых каталога с именами letters, memos, misk. Затем удалила эти каталоги одной командой.: *(рис 8.1)*

```sudo mkdir letters memos misk```;

```sudo rm -r letters memos misk```
 
 ![]()
 
*Рис 8.1. Создала три каталога и удалила их*

9.  Удалила ранее созданный каталог ```~/newdir``` командой ```rm```. Проверила, был ли каталог удалён.: *(рис 9.1)*

```sudo rm -r newdir```

```ls```
 
 ![]()
 
*Рис 9.1. Удалила каталог и проверила, был ли он удален*
 

10.	 С помощью командыman определила, какую опцию команды ```ls``` нужно использовать для просмотра содержимого не только указанного каталога, но и подката-
логов, входящих в него.: 

```man ls```;

``` ls -a```

![]()

*Рис 10.1. Команда man ls*


11.	С помощью команды ```man``` определила набор опций команды ```ls```, позволяющий отсортировать по времени последнего изменения выводимый список содержимого
каталога с развёрнутым описанием файлов *(рис 11.1)*: 

```man ls```;

```ls -```

![]()

*Рис 11.1. Команда man ls*


12.	 Используя команду ```man``` для просмотра описания следующих команд: ```cd```, ```pwd```, ```mkdir```, ```rmdir```, ```rm```. Пояснила основные опции этих команд: *(рис 12.1)*
 
 ```man cd```;
 
 ```man pwd```;
 
 ```man mkdir```;
 
 ```man rmdir```;
 
 ```man rm```;
 
 
 ![]()
 
*Рис 12.1. Команда man*


13.	Используя информацию, полученную при помощи команды history, выполнила модификацию и исполнение нескольких команд из буфера команд: *(рис 13.1 и рис 13.2, рис 13.3)*
 
 ```history```
 
 
 ![]()
 
*Рис 13.1. История*

```!1385:s/alF/F```

![]()

*Рис 13.2. Модификация*

```cd; ls; pwd```

![]()

*Рис 13.3. Исполнение нескольких команд из буфера команд*



**Вывод:**

В данной лабораторной работе, я приобрела практические навыки взаимодействия пользователя с системой посредством командной строки.


**Контрольные вопросы (лабораторная работа №5)**

*1. * 



*2.	*



*3.	*




*4.	* 


 
*5. * 



*6.	* 


*7.	* 




*8.	*




*9.	*



*10. *




*11. *




*12. *



*13. * 




Qt используется в среде KDE (Kool Desktop Environment).
