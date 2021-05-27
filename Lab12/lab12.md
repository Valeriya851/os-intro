---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №12"

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






# ***Программирование в командном процессоре ОС UNIX. Ветвления и циклы***

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

Весьма необходимой при программировании является команда ```getopts```, которая осуществляет синтаксический анализ командной строки, выделяя флаги, и используется для объявления переменных. Синтаксис команды следующий:

  ```getopts option-string  variable  [arg ... ]```
  
  *Флаги* — это опции командной строки, обычно помеченные знаком минус; Например, для команды ```ls``` флагом может являться ```-F```. Иногда флаги имеют аргументы, связанные с ними. Программы интерпретируют флаги, соответствующим образом изменяя своё поведение.
  
  Оператор выбора ```case``` реализует возможность ветвления на произвольное число ветвей. Эта возможность обеспечивается в большинстве современных языков программирования, предполагающих использование структурного подхода.
  
В обобщённой форме оператор выбора case выглядит следующим образом: 

```case имя in```

```шаблон1) список-команд;;```

```шаблон2) список-команд;;```

```...```

```esac```

[Источник](https://esystem.rudn.ru/pluginfile.php/1142517/mod_resource/content/2/008-lab_shell_prog_1.pdf)


# **Цель работы:**

Изучить основы программирования в оболочке ОС UNIX. Научится писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.



# **Описание результатов выполнения задания:**


1. Создала файл ```lab12.txt``` *(рис 2.1)*:

```touch lab12.txt```
 
 ![]()
 
*Рис 2.1. Создание файла ```lab12.txt```*


2.	Используя команды getopts grep, написала командный файл, который анализирует командную строку с ключами:

– -iinputfile — прочитать данные из указанного файла; 

– -ooutputfile — вывести данные в указанный файл;

– -pшаблон — указать шаблон для поиска;

– -C — различать большие и малые буквы;

– -n — выдавать номера строк. *(рис 2.1)*:
 
 ![]()

*Рис 1.1. Написала скрипт*

**Скрипт**

#!/bin/bash                               (*Командная оболочка Bash*)[Источник](https://losst.ru/napisanie-skriptov-na-bash)

while getopts "iopCBn" optletter          (*Использование оператора ```getopts```*)
 
do case $optletter in                     (*Оператор выбора ```case```*)

i)	cat $2;;                              (*Вывод содержимого файла*)

o)	cp $2 $3;;                            (*Вывод текста в другой файл*)

p)	grep $4 $2;;                          (*Поиск слова в файле*)

C)	grep -E '^[a-z]' $2;;                 (*Вывод всех слов начинающихся с маленькой буквы*)

B)	grep -E '^[A-Z]' $2;;                 (*Вывод всех слов начинающихся с большой буквы*)

n)	cat -n $2;;                           (*Вывод содержимого файла с пронумерованными строками*)

esac

done

3.  Сделала файл исполняемым *(рис 3.1)*: `

```chmod ugo+x lab12.txt```

![]()

*Рис 3.1. Исполняемый файл*


4.	Запуск скрипта: *(рис 4.1)*
 
 ```./lab12.txt```
 
![]()

*Рис 4.1. Запуск*



5.	Создала файл ```lab12.cpp``` *(рис 5.1)*:

```touch lab12.cpp```
 
 ![]()
 
*Рис 5.1. Создание файла ```lab12.cpp```*


6.	Написала на языке С++ программу, которая вводит число и определяет, является ли оно больше нуля, меньше нуля или равно нулю: *(рис 6.1)*

 ![]()
 
*Рис 6.1. Написанная программа*

**Код:**

#include <iostream>

using namespace std;

int main()

{int a;

cout << "Vvedite chislo: \n";               (*Запрашивает ввод числа*)

cin >> a;

if (a>0){

cout << a << " > 0" << endl;}

else if (a == 0){

cout << a << " = 0" << endl;}

else{

cout << a << " < 0" << endl;}

exit(a);

return 0;

}

7. Создала файл ```lab12.sh``` *(рис 7.1)*:

```touch lab12.sh```
 
 ![]()
 
*Рис 7.1. Создание файла ```lab12.sh```*

8.	Написала скрипт который запускает программу и вывод введенное число, анализирует с помощью команды ```$?``` *(рис 8.1)*: `

![]()

*Рис 8.1. Написанный скрипт*

**Скрипт**

#!/bin/bash                         (*Командная оболочка Bash*)

g++ -o lab12 lab12.cpp              (*Компиляция*)

./lab12                             (*Запуск программы*)

echo $?

echo "Vveli eto chislo^"

9. Запуск скрипта: *(рис 9.1)*
 
 ```./lab12.sh```
 
![]()

*Рис 9.1. Запуск*


10.	Создала файл ```l12.txt``` *(рис 10.1)*:

```touch l12.txt```
 
 ![]()
 
*Рис 10.1. Создание файла ```l12.txt```*

11.	Написала командный файл, создающий указанное число файлов, пронумерованных последовательно от 1 до N (например 1.tmp, 2.tmp, 3.tmp,4.tmp и т.д.). Этот же командный файл умеет удалять все созданные им файлы (если они существуют) *(рис 11.1)*:

 ![]()
 
*Рис 11.1. Создание командного файла*

**Командный файл:**

#!/bin/bash                         (*Командная оболочка Bash*)

start=1

end=$1

for((i+=start;i<=end;i++));

do touch $i.tmp                     (*Создает файлы пронумерованные по порядку*)

done

i=0

start_=0

end_=$2

for((i+=start;i<=end_;i++));

do rm -r $i.tmp                    (*Удаляет файлы пронумерованные по порядку*)

done


12.	Сделала файл исполняемым *(рис 12.1)*: `

```chmod ugo+x l12.txt```

![]()

*Рис 12.1. Исполняемый файл*

13. Запуск скрипта: *(рис 13.1)*
 
 ```./l12.txt```
 
 Создание: *(рис 13.1)*
 
![]()

*Рис 13.1. Создание файлов*

Проверка правильности выполнения: *(рис 13.2)*

![]()

*Рис 13.2. Проверка*

Удаление созданных файлов: *(рис 13.3)*

![]()

*Рис 13.3. Создание файлов*

Проверка правильности выполнения: *(рис 13.4)*

![]()

*Рис 13.4. Проверка*

14. Создала файл ```12.txt``` *(рис 14.1)*:

```touch 12.txt```
 
 ![]()
 
*Рис 14.1. Создание файла ```12.txt```*

15. Написала командный файл, который с помощью команды ```tar``` запаковывает в архив все файлы в указанной директории. Модифицировала его так, что запаковываются только те файлы, которые были изменены менее недели тому назад *(рис 15.1)*:

 ![]()
 
*Рис 15.1. Создание скрипта*

**Скрипт:**

#!/bin/bash                                                   (*Командная оболочка Bash*)

mkdir newfiles                                                (*Создание нового каталога*)

find $1 -type f -mtime -7 -exec cp -- "{}" ~/newfiles \;      (*Поиск файлов и копирование в новый каталог*)[Источник](https://rtfm.co.ua/komanda-find-i-eyo-opcii-v-primerax/)

tar czf archive.tar.gz newfiles                               (*Архивация*)


16. 	Сделала файл исполняемым *(рис 16.1)*: `

```chmod ugo+x 12.txt```

![]()

*Рис 16.1. Исполняемый файл*


17. Запуск скрипта: *(рис 17.1)*
 
 ```./12.txt```
 
 
![]()

*Рис 17.1. Запуск*

Проверка: *(рис 17.2)*

![]()

*Рис 17.2. Проверка*



# **Библиография:**

1. [Источник 1](https://esystem.rudn.ru/pluginfile.php/1142520/mod_resource/content/3/009-lab_shell_prog_2.pdf)
2. [Источник 2](https://esystem.rudn.ru/pluginfile.php/1142517/mod_resource/content/2/008-lab_shell_prog_1.pdf)
3. [Источник 3](https://losst.ru/napisanie-skriptov-na-bash)
4. [Источник 4](https://rtfm.co.ua/komanda-find-i-eyo-opcii-v-primerax/)



# **Вывод:**

В данной лабораторной работе, я изучила основы программирования в оболочке ОС UNIX. Научилась писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.



# **Контрольные вопросы (лабораторная работа №12)**

*1. Каково предназначение команды getopts?* 


*2.	Какое отношение метасимволы имеют к генерации имён файлов?*



*3.	Какие операторы управления действиями вы знаете?*



*4.	Какие операторы используются для прерывания цикла?* 


 
*5. Для чего нужны команды false и true?* 



*6. Что означает строка if test -f man$s/$i.$s, встреченная в командном файле?* 
 



*7.	Объясните различия между конструкциями while и until.* 


