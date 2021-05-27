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
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/1.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119786259-d0898000-bef1-11eb-99d7-fd4a840cd2d5.png))
 
*Рис 2.1. Создание файла ```lab12.txt```*


2.	Используя команды getopts grep, написала командный файл, который анализирует командную строку с ключами:

– -iinputfile — прочитать данные из указанного файла; 

– -ooutputfile — вывести данные в указанный файл;

– -pшаблон — указать шаблон для поиска;

– -C — различать большие и малые буквы;

– -n — выдавать номера строк. *(рис 2.1)*:
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/2.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119786418-fb73d400-bef1-11eb-9d5c-79b59de0bba8.png))

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

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/3.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119786467-0890c300-bef2-11eb-94cd-740fd72db846.png))

*Рис 3.1. Исполняемый файл*


4.	Запуск скрипта: *(рис 4.1)*
 
 ```./lab12.txt```
 
![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/4.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119786570-26f6be80-bef2-11eb-8db5-0640dcc4500c.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/5.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119786644-383fcb00-bef2-11eb-8f23-5d842f0c7657.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/6.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119786701-442b8d00-bef2-11eb-8e72-14708584190b.png))

*Рис 4.1. Запуск*



5.	Создала файл ```lab12.cpp```:

```touch lab12.cpp```


6.	Написала на языке С++ программу, которая вводит число и определяет, является ли оно больше нуля, меньше нуля или равно нулю: *(рис 6.1)*

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/7.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119786751-51487c00-bef2-11eb-9bcf-62c1e95a74f8.png))
 
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

7. Создала файл ```lab12.sh```:

```touch lab12.sh```
 
 

8.	Написала скрипт который запускает программу и вывод введенное число, анализирует с помощью команды ```$?``` *(рис 8.1)*: `

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/8.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119786800-5c9ba780-bef2-11eb-89a8-3251da9ba832.png))

*Рис 8.1. Написанный скрипт*

**Скрипт**

#!/bin/bash                         (*Командная оболочка Bash*)

g++ -o lab12 lab12.cpp              (*Компиляция*)

./lab12                             (*Запуск программы*)

echo $?

echo "Vveli eto chislo^"

9. Запуск скрипта: *(рис 9.1)*
 
 ```./lab12.sh```
 
![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/9.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119786851-68876980-bef2-11eb-81ff-4bc8bec999ed.png))

*Рис 9.1. Запуск*


10.	Создала файл ```l12.txt```:

```touch l12.txt```

11.	Написала командный файл, создающий указанное число файлов, пронумерованных последовательно от 1 до N (например 1.tmp, 2.tmp, 3.tmp,4.tmp и т.д.). Этот же командный файл умеет удалять все созданные им файлы (если они существуют) *(рис 11.1)*:

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/10.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119786888-750bc200-bef2-11eb-9a6d-1469ecfdf3f5.png))
 
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


12.	Сделала файл исполняемым: `

```chmod ugo+x l12.txt```


13. Запуск скрипта: *(рис 13.1)*
 
 ```./l12.txt```
 
 Создание: *(рис 13.1)*
 
![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/11.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119786939-81901a80-bef2-11eb-9475-a42d5c10144b.png))

*Рис 13.1. Создание файлов*

Проверка правильности выполнения: *(рис 13.2)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/12.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119786982-8c4aaf80-bef2-11eb-9c77-28415abdb0a7.png))

*Рис 13.2. Проверка*

Удаление созданных файлов: *(рис 13.3)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/13.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119787023-966cae00-bef2-11eb-9d4c-ea10853b04a5.png))

*Рис 13.3. Создание файлов*

Проверка правильности выполнения: *(рис 13.4)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/14.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119787067-a08eac80-bef2-11eb-8420-c4929d628140.png))

*Рис 13.4. Проверка*

14. Создала файл ```12.txt```:

```touch 12.txt```

15. Написала командный файл, который с помощью команды ```tar``` запаковывает в архив все файлы в указанной директории. Модифицировала его так, что запаковываются только те файлы, которые были изменены менее недели тому назад *(рис 15.1)*:

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/15.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119787101-a97f7e00-bef2-11eb-90f3-c515b406c991.png))
 
*Рис 15.1. Создание скрипта*

**Скрипт:**

#!/bin/bash                                                   (*Командная оболочка Bash*)

mkdir newfiles                                                (*Создание нового каталога*)

find $1 -type f -mtime -7 -exec cp -- "{}" ~/newfiles \;      (*Поиск файлов и копирование в новый каталог*)[Источник](https://rtfm.co.ua/komanda-find-i-eyo-opcii-v-primerax/)

tar czf archive.tar.gz newfiles                               (*Архивация*)


16. 	Сделала файл исполняемым: `

```chmod ugo+x 12.txt```


17. Запуск скрипта: *(рис 17.1)*
 
 ```./12.txt```
 
![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/16.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119787136-b603d680-bef2-11eb-9ad8-8cdb0a97f824.png))

*Рис 17.1. Запуск*

Проверка: *(рис 17.2)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/17.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119787165-bf8d3e80-bef2-11eb-88b1-c1fc9e5a4da4.png))

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

Весьма необходимой при программировании является команда ```getopts```, которая осуществляет синтаксический анализ командной строки, выделяя флаги, и используется для объявления переменных. Синтаксис команды следующий:

  ```getopts option-string  variable  [arg ... ]```
  
*2.	Какое отношение метасимволы имеют к генерации имён файлов?*

При перечислении имён файлов текущего каталога можно использовать следующие символы:

– * — соответствует произвольной, в том числе и пустой строке;

– ? — соответствует любому одинарному символу;

– [c1-c1] — соответствует любому символу, лексикографически находящемусямежду символами c1 и с2. 

– echo * — выведет имена всех файлов текущего каталога, что представляет собой простейший аналог команды ls;

– ls *.c — выведет все файлы с последними двумя символами, совпадающими с .c.

– echo prog.? — выведет все файлы, состоящие из пяти или шести символов, первыми пятью символами которых являются prog..

– [a-z]* — соответствует произвольному имени файла в текущем каталоге, на- чинающемуся с любой строчной буквы латинского алфавита.

Такие символы, как ' < > * ? | \ " &, являются метасимволами и имеют для командного процессора специальный смысл. Снятие специального смысла с метасимвола называется экранированием метасимвола. Экранирование может быть осуществлено с помощью предшествующего метасимволу символа \, который, в свою очередь, является метасимволом.

Для экранирования группы метасимволов нужно заключить её в одинарные кавычки. Строка, заключённая в двойные кавычки, экранирует все метасимволы, кроме $, ' , \, ". Например,

– echo \* выведет на экран символ *,

– echo ab’*\|*’cd выведет на экран строку ab*\|*cd.


*3.	Какие операторы управления действиями вы знаете?*

Часто бывает необходимо обеспечить проведение каких-либо действий циклически и управление дальнейшими действиями в зависимости от результатов проверки некоторого условия. Для решения подобных задач язык программирования bash предоставляет возможность использовать такие управляющие конструкции, как for, case, if и while. С точки зрения командного процессора эти управляющие конструкции являются обычными командами и могут использоваться как при создании командных файлов, так и при работе в интерактивном режиме. Команды, реализующие подобные конструкции, по сути, являются операторами языка программирования bash. Поэтому при описании языка программирования bash термин оператор будет использоваться наравне с термином команда.

Команды ОС UNIX возвращают код завершения, значение которого может быть использовано для принятия решения о дальнейших действиях. Команда test, например, создана специально для использования в командных файлах. Единственная функция этой команды заключается в выработке кода завершения.

Оператор выбора ```case``` реализует возможность ветвления на произвольное число ветвей. Эта возможность обеспечивается в большинстве современных языков программирования, предполагающих использование структурного подхода.
  
В обобщённой форме оператор выбора case выглядит следующим образом: 

```case имя in```

```шаблон1) список-команд;;```

```шаблон2) список-команд;;```

```...```

```esac```

В обобщённой форме условный оператор if выглядит следующим образом: 

```if список-команд```

```then список-команд```

```{elif список-команд```

```then список-команд}```

```[else список-команд]```

```fi```

Выполнение условного оператора if сводится к тому, что сначала выполняется последовательность команд (операторов), которую задаёт список-команд в строке, содержащей служебное слово if. 

*4.	Какие операторы используются для прерывания цикла?* 

Два несложных способа позволяют вам прерывать циклы в оболочке bash. Команда break завершает выполнение цикла, а команда continue завершает данную итерацию блока операторов.

Команда break полезна для завершения цикла while в ситуациях, когда условие перестаёт быть правильным. Пример бесконечного цикла while с прерыванием в момент, когда файл перестаёт существовать:

```while true do```

```if [! -f $file] then```

```break```

```fi```

```sleep 10 done```

 
*5. Для чего нужны команды false и true?* 

Команда true - всегда возвращает код завершения, равный 0 (истина);

Команда false - всегда возвращает код завершения, не равный 0 (ложь).

Логиический тип данных — примитивный тип данных в информатике, принимающий два возможных значения, иногда называемых истиной (true) и ложью (false).


*6. Что означает строка if test -f man$s/$i.$s, встреченная в командном файле?* 
 
test -f - истина, если файл существует;

Команды ОС UNIX возвращают код завершения, значение которого может быть использовано для принятия решения о дальнейших действиях. Команда test, например, создана специально для использования в командных файлах. Единственная функция этой команды заключается в выработке кода завершения. Так например, команда

test -f file

При использовании где-либо в команд- ном файле комбинации символов $i, где 0 < i < 10, вместо неё будет осуществлена подстановка значения параметра с порядковым номером i, т.е. аргумента команд- ного файла с порядковым номером i. 

/ - делит;


*7.	Объясните различия между конструкциями while и until.* 

until запускает цикл до тех пор, пока условие не станет истинным (то есть пока условие не станет ложным).

While Loop выполняет блок кода (заключенный в do... done), когда условие истинно , и продолжает выполнять его до тех пор, пока условие не станет ложным .

Они противоположны:
while(b) = until(!b)
