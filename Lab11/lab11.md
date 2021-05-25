---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №11"

author: "Тулеева Валерия, НБИбд-01-20"

# Formatting
toc_depth: 2
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







# ***Программирование в командном процессоре ОС UNIX. Командные файлы***

# **Оглавление:**

1.	Введение:
  a) Цель работы
2.	Описание результатов выполнения задания;
3.	Вывод;
4.	Библиография;
5.	Контрольные вопросы.

























# **Введение:**

*Командный процессор* (командная оболочка, интерпретатор команд shell) — это программа, позволяющая пользователю взаимодействовать с операционной системой компьютера. В операционных системах типа UNIX/Linux наиболее часто используются следующие реализации командных оболочек:

– *оболочка Борна* (Bourne shell или sh) — стандартная командная оболочка UNIX/Linux, содержащая базовый, но при этом полный набор функций;

– *С-оболочка* (или csh) — надстройка на оболочкой Борна, использующая С- подобный синтаксис команд с возможностью сохранения истории выполнения команд;

– *оболочка Корна *(или ksh) — напоминает оболочку С, но операторы управления программой совместимы с операторами оболочки Борна;

– *BASH* — сокращение от Bourne Again Shell (опять оболочка Борна), в основе своей совмещает свойства оболочек С и Корна (разработка компании Free Software Foundation).

*POSIX* (Portable Operating System Interface for Computer Environments) — набор стандартов описания интерфейсов взаимодействия операционной системы и прикладных программ. [Источник](https://esystem.rudn.ru/pluginfile.php/1142517/mod_resource/content/2/008-lab_shell_prog_1.pdf)


# **Цель работы:**

Изучить основы программирования в оболочке ОС UNIX/Linux. Научиться писать небольшие командные файлы.



# **Описание результатов выполнения задания:**


1.  Изучила информацию о ```zip```, ```tar```, ```bzip2``` , вызвав в командной строке ```man ...```*(рис 1.1 и 1.2, 1.3, 1.4, 1.5, 1.6)*:


 ```man zip```; *(рис 1.1 и рис 1.2)*
 
 ![]()
 
 ![]()
 
 *Рис 1.1 и 1.2. Команда man zip*
 
 
 ```man bzip2```; *(рис 1.3 и рис 1.4)*
 

 ![]()
 
 ![]()
 
 *Рис 1.3 и 1.4. Команда man bzip2*
 
 
 ```man tar```; *(рис 1.5 и рис 1.6 )*

 ![]()
 
 ![]()
 
 *Рис 1.5 и 1.6. Команда man tar*
 

2.	 Создала файл ```lab11.txt``` *(рис 2.1)*:

```touch lab11.txt```
 
 ![]()
 
*Рис 2.1. Создание файла ```lab11.txt```*



3.	Написала скрипт, который при запуске будет делать резервную копию самого себя (то есть файла, в котором содержится его исходный код) в другую директорию backup в домашнем каталоге. При этом файл архивируется архиватором tar *(рис 3.1)* :

![]()

*Рис 3.1. Написала скрипт*

**Скрипт**

 #!/bin/bash                                                    (*Командная оболочка Bash*)
 
cp lab11.txt backup                                             (*Копирование файла с кодом в директорию*)

echo "Файл с исходным кодом скопирован в директорию backup".    (*Вывод на экран строки*)

tar --totals -cvf archive.tar lab11.txt                         (*С помощью этой команды создается архив*) [Источник](https://losst.ru/komanda-tar-v-linux)

echo "Архивация файла"                                          (*Вывод на экран строки*)


4.  Сделала файл исполняемым *(рис 4.1)*: `

```chmod ugo+x lab11.txt```

![]()

*Рис 4.1. Исполняемый файл*


5.	Запуск скрипта: *(рис 5.1)*
 
 ```./lab11.txt```
 
![]()

*Рис 5.1. Запуск*



6.	Создала файл ```lab.txt``` *(рис 6.1)*:

```touch lab.txt```
 
 ![]()
 
*Рис 6.1. Создание файла ```lab.txt```*


7.	Написала пример командного файла, обрабатывающего любое произвольное число аргументов командной строки, в том числе превышающее десять. Скрипт может последовательно распечатывать значения всех переданных аргументов: *(рис 7.1)*

 ![]()
 
*Рис 7.1. Написанный скрипт*

**Скрипт:**

#!/bin/bash                          (*Командная оболочка Bash*)

echo $1

echo $2

echo $3                              (*Позиционные аргументы сценария*)

echo $4

echo $5

echo $6                 

echo $7

echo $8

echo $9

echo ${10}

echo ${11}

8.	Сделала файл исполняемым *(рис 8.1)*: `

```chmod ugo+x lab.txt```

![]()

*Рис 8.1. Исполняемый файл*

9. Запуск скрипта: *(рис 9.1 и 9.2)*
 
 ```./lab.txt```
 
 Несколько переменных:
 
![]()

*Рис 9.1. Запуск*

11 переменных:

![]()

*Рис 9.2. Запуск*

10.	Создала файл ```lb.txt``` *(рис 10.1)*:

```touch lb.txt```
 
 ![]()
 
*Рис 10.1. Создание файла ```lb.txt```*

11.	Написала командный файл — аналог команды ```ls``` *(рис 11.1)*:

 ![]()
 
*Рис 11.1. Создание скрипта*

**Скрипт:**

#!/bin/bash                       (*Командная оболочка Bash*)

for file in *

do                                (*Делается*)

echo -n $file:""

pwd 

done                              (*Сделано*)


12.	Сделала файл исполняемым *(рис 12.1)*: `

```chmod ugo+x lb.txt```

![]()

*Рис 12.1. Исполняемый файл*

13. Запуск скрипта: *(рис 13.1)*
 
 ```./lb.txt```
 
 Ввела ```/home``` 
 
![]()

*Рис 13.1. Запуск*


14. Создала файл ```l.txt``` *(рис 14.1)*:

```touch l.txt```
 
 ![]()
 
*Рис 14.1. Создание файла ```l.txt```*

15. Написала командный файл, который получает в качестве аргумента командной строки формат файла (.txt, .doc, .jpg, .pdf и т.д.) и вычисляет количество таких файлов в указанной директории. Путь к директории также передаётся в виде аргумента командной строки.

 ![]()
 
*Рис 15.1. Создание скрипта*

**Скрипт:**

#!/bin/bash                            (*Командная оболочка Bash*)

echo $1                                (*Позиционные аргументы сценария*)

echo $2 

find $2 -name "*$1" -print             (*поиск файла с определенным файлом*)

tree -P "*$1" --prune $2               (*Выводит информацию, считает сколько файлов и директорий есть с таким форматом*)[Источник](https://losst.ru/komanda-tree-linux)


16. 	Сделала файл исполняемым *(рис 16.1)*: `

```chmod ugo+x l.txt```

![]()

*Рис 16.1. Исполняемый файл*


17. Запуск скрипта: *(рис 17.1 и 17.2)*
 
 ```./lb.txt```
 
 Ввела ```.txt``` ```~```
 
![]()

*Рис 17.1. Запуск*

Ввела ```.pdf``` ```~```

![]()

*Рис 17.2. Запуск*



# **Библиография:**

1. [Источник 1](https://esystem.rudn.ru/pluginfile.php/1142517/mod_resource/content/2/008-lab_shell_prog_1.pdf)
2. [Источник 2](https://losst.ru/komanda-tar-v-linux)
3. [Источник 3](https://losst.ru/komanda-tree-linux)



# **Вывод:**

В данной лабораторной работе, я изучила основы программирования в оболочке ОС UNIX/Linux. Научилась писать небольшие командные файлы.



# **Контрольные вопросы (лабораторная работа №11)**

*1. Объясните понятие командной оболочки. Приведите примеры командных обо- лочек. Чем они отличаются?* 


*2.	Что такое POSIX?*

*POSIX* (Portable Operating System Interface for Computer Environments) — набор стандартов описания интерфейсов взаимодействия операционной системы и прикладных программ. 

*3.	Как определяются переменные и массивы в языке программирования bash?*





*4.	Каково назначение операторов let и read?* 


 
*5. Какие арифметические операции можно применять в языке программирования bash?* 



*6. Что означает операция (( )) ?* 
 



*7.	Какие стандартные имена переменных Вам известны?* 



*8.	Что такое метасимволы?*




*9. Как экранировать метасимволы?*


*10. Как создавать и запускать командные файлы?*


*11. Как определяются функции в языке программирования bash?*


*12. Каким образом можно выяснить, является файл каталогом или обычным файлом?*

*13. Каково назначение команд set, typeset и unset?*

*14. Как передаются параметры в командные файлы?*


*15. Назовите специальные переменные языка bash и ихназначение.*
