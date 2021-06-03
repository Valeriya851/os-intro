---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №13"

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







# ******

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

Изучить основы программирования в оболочке ОС UNIX. Научиться писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.

# **Описание результатов выполнения задания:**

1. Создала файл ```lab13.txt```:

```touch lab13.txt```


2.	Реализовала команду man с помощью командного файла. Изучила содержимое каталога /usr/share/man/man1. В нем находятся архивы текстовых файлов, содержащих справку по большинству установленных в системе программ и команд. Каждый архив можно открыть командой less сразу же просмотрев содержимое справки. Командный файл получает в виде аргумента командной строки название команды и в виде результата выдает справку об этой команде или сообщение об отсутствии справки, если соответствующего файла нет в каталоге man1*(рис 2.1)*:
 
 ![]()

*Рис 1.1. Написала скрипт*

**Скрипт**

#!/bin/bash                       (*Командная оболочка Bash*)

cd /usr/share/man/man1

ls

for file in *

do

   less "$file"
   
   man $1
   
   break
   
done

3.  Сделала файл исполняемым *(рис 3.1)*: `

```chmod ugo+x lab13.txt```

![]()

*Рис 3.1. Исполняемый файл*


4.	Запуск скрипта: *(рис 4.1)*
 
 ```./lab13.txt```
 
![]()

![]()

![]()

*Рис 4.1. Запуск*

**Отдельный командный файл для запуска команды ```less```** *(рис 4.2)*:

```touch dz.txt```

```chmod ugo+x dz.txt```

```./dz.txt```

![]()

![]()

![]()

*Рис 4.2. Запуск*

**Скрипт**

#!/bin/bash                   (*Командная оболочка Bash*)

cd /usr/share/man/man1

ls

for file in *

do

   less "$file"             (*Просмотр содержимого*)

done

**Отдельный командный файл для запуска команды ```man```** *(рис 4.3)*:

```touch dz1.txt```

```chmod ugo+x dz1.txt```

```./dz1.txt```

![]()

![]()

![]()

*Рис 4.3. Запуск*

**Скрипт**

#!/bin/bash                   (*Командная оболочка Bash*)

cd /usr/share/man/man1

ls

for file in *

do

   man $1                  (*Команда man*)
   
break

done

5.	Создала файл ```a.txt```:

```touch a.txt```


6.	Используя встроенную переменную $RANDOM, написала командный файл, генерирующий случайную последовательность букв латинского алфавита. *(рис 6.1)*

 ![]()
 
*Рис 6.1. Написанная программа*

**Скрипт:**

#!/bin/bash                                               (*Командная оболочка Bash*)

head /dev/urandom | tr -dc A-Za-z | head -c 13; echo ''    (*Генерация рандомных букв*)

Запустила программу:

```chmod ugo+x a.txt```

```./a.txt``` *(рис 6.2)*

![]()

*Рис 6.2. Запуск*

7. Создала файл ```b.txt```:

```touch b.txt```


8.	Написала командный файл. Командный файл в течение некоторого времени t1 дожидаться освобождения ресурса, выдавая об этом сообщение, а дождавшись его освобождения, использует его в течение некоторого времени t2. Запустила командный файл в одном виртуальном терминале в фоновом режиме, перенаправив его вывод в другой (> /dev/tty#, где # — номер терминала куда перенаправляется вывод), в котором также запущен этот файл, но не фоновом, а в привилегированном режиме.  *(рис 8.1)*: `

![])

*Рис 8.1. Написанный скрипт*

**Скрипт**

#!/bin/bash                            (*Командная оболочка Bash*)

echo $1

echo $2=t1

echo "t1 v techenii etogo vremeni"

echo $3=t2

echo "resyrs ecpolzyetca"

./$1&

sudo -s ./$1 > /dev/tty2             (*Перенаправка вывода*)

echo "zapeshen etot fail $1" 


9. Запуск скрипта: *(рис 9.1)*
 
 ```chmod ugo+x b.txt```
 
 ```./b.txt```
 
![]()

*Рис 9.1. Запуск*


10.	Создала файл ```lab12.sh```:

```touch l12.txt```

**Скрипт:** *(рис 10.1)*

#!/bin/bash                 (*Командная оболочка Bash*)

g++ -o lab13 lab13.c        (*Запуск файла*)

./lab13

 ![]()
 
*Рис 10.1. Скрипт* 

**Командный файл** *(рис 10.2)*

```touch lab13.c```

struct semaphore          

     {      
     
        int val[NUMPROCS];  
        
        int lastid;      
        
     };          
     
     int procid;     
     
     int lastid;                 
                                                                
     INIT(semaphore)            
     
        struct semaphore semaphore;      
        
     {                         
     
        int i;        
        
        for (i = 0; i < NUMPROCS; i++)   
        
             semaphore.val[i] = 0;  
             
     }            
     
     Pprim(semaphore)   
     
        struct semaphore semaphore;    
        
     {                     
     
        int i,first;     
        
                                                                
      loop:          
      
        first = lastid;  
        
        semaphore.val[procid] = 1;   
        
        forloop:             
        
        for (i = first; i < NUMPROCS; i++)  
        
        {               
        
             if (i == procid)     
             
             {        
             
                 semaphore.val[i] = 2;     
                 
                 for (i = 1; i < NUMPROCS; i++)    
                 
                      if (i != procid && semaphore.val[i] == 2) 
                      
                          goto loop;         
                          
                 lastid = procid;      
                 
                 return;          
                 
             }             
             
             else if (semaphore.val[i])  
             
                 goto loop;         
                 
        }           
        
        first = 1; 
        
        goto forloop;     
        
     }  
     
     Vprim(semaphore)   
     
        struct semaphore semaphore;    
        
     {                 
     
        lastid = (procid + 1) % NUMPROCS; 
        
        semaphore.val[procid] = 0;       
        
     }                

![])

![])

*Рис 10.2. Написанный скрипт*



# **Вывод:**

В данной лабораторной работе, я изучила основы программирования в оболочке ОС UNIX. Научилась писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.

# **Библиография:**

1. [Источник 1](https://esystem.rudn.ru/pluginfile.php/1142523/mod_resource/content/2/010-lab_shell_prog_3.pdf)
2. [Источник 2](https://esystem.rudn.ru/pluginfile.php/1142517/mod_resource/content/2/008-lab_shell_prog_1.pdf)


# **Контрольные вопросы (лабораторная работа №13)**

*1. Найдите синтаксическую ошибку в следующей строке:* 
while [$1 != "exit"]

*2.	Как объединить (конкатенация) несколько строк в одну?*



*3.	Найдите информацию об утилите seq. Какими иными способами можно реализовать её функционал при программировании на bash?*





*4.	 Какой результат даст вычисление выражения $((10/3))?* 


 
*5. Укажите кратко основные отличия командной оболочки zsh от bash.* 



*6. Проверьте, верен ли синтаксис данной конструкции for ((a=1; a <= LIMIT; a++))* 
 



*7.	Сравните язык bash с какими-либо языками программирования. Какие преимущества у bash по сравнению с ними? Какие недостатки?* 




