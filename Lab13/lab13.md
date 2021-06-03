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







# ***Программирование в командном процессоре ОС UNIX. Расширенное программирование***

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
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/7.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631288-8708da00-c489-11eb-9291-d666d7d366b5.png))

*Рис 1.1. Написала скрипт*

**Скрипт**

```#!/bin/bash```                     (*Командная оболочка Bash*)

```cd /usr/share/man/man1```

```ls```

```for file in *```

```do```

  ``` less "$file"```
   
   ```man $1```
   
   ```break```
   
```done```

3.  Сделала файл исполняемым *(рис 3.1)*: `

```chmod ugo+x lab13.txt```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/9.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631352-9a1baa00-c489-11eb-92a3-ea2756d12b11.png))

*Рис 3.1. Исполняемый файл*


4.	Запуск скрипта: *(рис 4.1)*
 
 ```./lab13.txt```
 
![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/10.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631391-a56ed580-c489-11eb-99ee-38318d01c544.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/11.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631426-af90d400-c489-11eb-877a-45e3266e1ddb.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/13.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631527-cdf6cf80-c489-11eb-8bfb-9524bdfc2fe1.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/14.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631564-d7803780-c489-11eb-8f1f-5891eca66eb9.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/15.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631628-e8c94400-c489-11eb-946b-48bb7e5d8903.png))


*Рис 4.1. Запуск*

**Отдельный командный файл для запуска команды ```less```** *(рис 4.2)*:

```touch dz.txt```

```chmod ugo+x dz.txt```

```./dz.txt```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/16.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631719-ff6f9b00-c489-11eb-8ecb-59ecf74c08e5.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/17.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631756-08f90300-c48a-11eb-9ff1-7b181ad35ec4.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/18.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631795-17dfb580-c48a-11eb-9b22-fcd8e60c153c.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/19.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631836-2037f080-c48a-11eb-8837-c9ad16bfb231.png))

*Рис 4.2. Запуск*

**Скрипт**

```#!/bin/bash```                   (*Командная оболочка Bash*)

```cd /usr/share/man/man1```

```ls```

```for file in *```

```do```

   ```less "$file"```            (*Просмотр содержимого*)

```done```

**Отдельный командный файл для запуска команды ```man```** *(рис 4.3)*:

```touch dz1.txt```

```chmod ugo+x dz1.txt```

```./dz1.txt```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/20.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631866-2a59ef00-c48a-11eb-85b6-e601746bb1ce.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/21.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631897-334ac080-c48a-11eb-88f0-0ae8dc885fdd.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/22.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631926-3f368280-c48a-11eb-900b-9e66ca0fc0ae.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/23.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631965-48bfea80-c48a-11eb-8b30-e6ec65c422eb.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/24.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120632033-5a08f700-c48a-11eb-8993-212c002ed69f.png))

*Рис 4.3. Запуск*

**Скрипт**

```#!/bin/bash```                   (*Командная оболочка Bash*)

```cd /usr/share/man/man1```

```ls```

```for file in *```

```do```

   ```man $1```                 (*Команда man*)
   
```break```

```done```

5.	Создала файл ```a.txt```:

```touch a.txt```


6.	Используя встроенную переменную $RANDOM, написала командный файл, генерирующий случайную последовательность букв латинского алфавита. *(рис 6.1)*

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/26.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120632158-7c027980-c48a-11eb-865e-1c330be80bba.png))
 
*Рис 6.1. Написанная программа*

**Скрипт:**

```#!/bin/bash```                                              (*Командная оболочка Bash*)

```head /dev/urandom | tr -dc A-Za-z | head -c 13; echo ''```    (*Генерация рандомных букв*)

Запустила программу:

```chmod ugo+x a.txt```

```./a.txt``` *(рис 6.2)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/25.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120632097-6d1bc700-c48a-11eb-9ee2-f32c5a988c7b.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/27.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120632287-9c323880-c48a-11eb-92d5-e6b156966f5f.png))

*Рис 6.2. Запуск*

7. Создала файл ```b.txt```:

```touch b.txt```


8.	Написала командный файл. Командный файл в течение некоторого времени t1 дожидаться освобождения ресурса, выдавая об этом сообщение, а дождавшись его освобождения, использует его в течение некоторого времени t2. Запустила командный файл в одном виртуальном терминале в фоновом режиме, перенаправив его вывод в другой (> /dev/tty#, где # — номер терминала куда перенаправляется вывод), в котором также запущен этот файл, но не фоновом, а в привилегированном режиме.  *(рис 8.1)*: `

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/1.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631004-32655f00-c489-11eb-839a-45f4cba210bc.png))

*Рис 8.1. Написанный скрипт*

**Скрипт**

```#!/bin/bash```                            (*Командная оболочка Bash*)

```echo $1```

```echo $2=t1```

```echo "t1 v techenii etogo vremeni"```

```echo $3=t2```

```echo "resyrs ecpolzyetca"```

```./$1&```

```sudo -s ./$1 > /dev/tty2```             (*Перенаправка вывода*)

```echo "zapeshen etot fail $1"``` 


9. Запуск скрипта: *(рис 9.1)*
 
 ```chmod ugo+x b.txt```
 
 ```./b.txt```
 
![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/2.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631062-4315d500-c489-11eb-8201-858e0ef7d4f2.png))

*Рис 9.1. Запуск*


10.	Создала файл ```lab12.sh```:

```touch l12.txt```

**Скрипт:** *(рис 10.1)*

#!/bin/bash                 (*Командная оболочка Bash*)

g++ -o lab13 lab13.c        (*Запуск файла*)

./lab13

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/6.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631224-76586400-c489-11eb-8a01-5eb3aa092bca.png))
 
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

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/3.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631124-532db480-c489-11eb-9802-8edf586df411.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/4.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631154-5c1e8600-c489-11eb-8bdd-c0038459854b.png))

*Рис 10.2. Написанный скрипт*



# **Вывод:**

В данной лабораторной работе, я изучила основы программирования в оболочке ОС UNIX. Научилась писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.

# **Библиография:**

1. [Источник 1](https://esystem.rudn.ru/pluginfile.php/1142523/mod_resource/content/2/010-lab_shell_prog_3.pdf)
2. [Источник 2](https://esystem.rudn.ru/pluginfile.php/1142517/mod_resource/content/2/008-lab_shell_prog_1.pdf)


# **Контрольные вопросы (лабораторная работа №13)**

*1. Найдите синтаксическую ошибку в следующей строке:* 
while [$1 != "exit"]

Ответ:

while ["$1" != "exit"]

*2.	Как объединить (конкатенация) несколько строк в одну?*

Самый простой способ объединить две или более строковые переменные – записать их одну за другой:

VAR1="Hello,"

VAR2=" World"

VAR3="$VAR1$VAR2"

echo "$VAR3"

Вывод:

Hello, World

Вы также можете объединить одну или несколько переменных с литеральными строками:

VAR1="Hello,"

VAR2="${VAR1}World"

echo "$VAR2"

Вывод:

Hello, World

*3.	Найдите информацию об утилите seq. Какими иными способами можно реализовать её функционал при программировании на bash?*

seq

Эта утилиты выводят последовательность целых чисел с шагом, заданным пользователем.

По-умолчанию, выводимые числа отделяются друг от друга символом перевода строки, однако, с помощью ключа -s может быть задан другой разделитель.

bash$ seq 5
1
2
3
4
5



bash$ seq -s : 5
1:2:3:4:5
             


Утилита seq очень удобно использовать для генерации списка аргументов в цикле for.


*4.	 Какой результат даст вычисление выражения $((10/3))?* 

Арифметическое расширение POSIX для целочисленной арифметики

 
*5. Укажите кратко основные отличия командной оболочки zsh от bash.* 

Z Shell

Zsh, или Z Shell впервые выпустил Paul Falstad (Пол Фалстад) в 1990 году, когда он ещё был студентом Принстонского университета. Z Shell входит во многие операционные системы, в том числе и в Mac OS (хотя она там не установлена по умолчанию).

Подобно Bash, Z Shell можно в общем рассматривать как расширенную версию Bourne Shell, и она содержит много черт, сходных с Bash, что вы сможете заметить ниже. Также можно видеть, что она довольно сильно напоминает Korn Shell. Некоторые возможности, о которых стоит упомянуть (но не все):

Шаблоны поиска файлов

Исправление правописания

Краткие имена директорий (например, ~ или ..)

Загружаемые модули, наподобие контроля сокетов или FTP клиента

Режимы совместимости (например, вы можете использовать /bin/bash как замену Bash)

Скрипты запуска/выключения через zshenv, zprofile, zshrc, zlogin и zlogout

Завершение команд git

Расширение путей: например, введите cd /u/lo/b, нажмите Tab, и путь будет завершён в виде cd /usr/local/bin, поскольку это единственный подходящий путь.



Bash

Оболочка Bash (также известная как «Bourne-again shell» — «снова оболочка Борна» или «рождённая вновь оболочка») была выпущена примерно в то же время, что и Z Shell (в 1989 году), её создателем считается Brian Fox (Брайан Фокс). Она была изначально написана как замена Bourne Shell. Через несколько лет она стала основной оболочкой для GNU, большинства дистрибутивов Linux и Mac OS (версии 10.3+). Как и положено настоящему последователю, Bash способен без проблем исполнять все команды Bourne Shell.

Вот несколько особенностей, которыми обладает оболочка Bash, включая и менее известные:

Вставка заключилельных параметров предыдущей команды в текущую, используя Alt + .

Вы можете продолжать исполнять процесс даже после выхода. Чтобы это сделать, воспользуйтесь командой disown -h <pid>, где вместо <pid> нужно указать номер процесса.
  
Вновь запустить предыдущую команду через sudo, применяя sudo !! (!! — это обозначение для предшествующей команды).


Выполнить обратный инкрементальный поиск с помощью клавиш Ctrl + R.

Нажмите клавишу Tab дважды, и вы получите список возможных дополнений для слова, которое вы только что ввели или вводите.

Когда исполняете скрипт в Bash, опция -x выведет его содержимое, как при запуске.

*6. Проверьте, верен ли синтаксис данной конструкции for ((a=1; a <= LIMIT; a++))* 
 
Пример:

for ((a=1; a<10; a++))


*7.	Сравните язык bash с какими-либо языками программирования. Какие преимущества у bash по сравнению с ними? Какие недостатки?* 

**Bash**

Наиболее часто используемая командная оболочка по умолчанию в операционных системах GNU/Linux. Она включает в себя простой язык программирования, который позволяет при помощи условных операторов и операторов цикла использовать утилиты и программы операционной системы для написания как простых, так и сложных скриптов. 

В этом плане Bash, несомненно, обладает некоторыми преимуществами, в частности, универсальностью и доступностью. Для того, чтобы написать скрипт на Bash, установка дополнительных пакетов не требуется. Достаточно создать файл вида script_name.sh с последовательно исполняемыми операциями и запустить его, либо добавить в качестве задачи планировщика cron.  

Вот далеко не полный список задач, которые можно решить с использованием bash-скрипта:

– вывод нескольких последних строк лога или поиск и выборка ключевых слов с последующим сохранением в отдельный файл;

– архивирование каталога с данными с последующей отправкой архива на удаленный компьютер по ssh или telnet;

– настройка системы бэкапа файлов базы данных с использованием дампинга;

– запрос информации о конфигурации нескольких компьютеров в сети и отправка файла с результатами по e-mail;

– поиск дубликатов файлов на диске с последующим выводом списка имен и запросом на удаление;

– рекурсивная замена владельцев отдельных файлов и каталогов на диске.

Стоит отметить, что возможности командного интерпретатора зачастую используются не полностью. Многие администраторы выбирают Bash для написания простых или средних по сложности скриптов. В крупных проектах, где есть специфические задачи и требуется работа с разнообразными входными данными, многомерными массивами и сокетами больше доверяют Perl, Python или Ruby. 

Отчасти это связано с проблемами переносимости bash-скриптов на другие платформы, (например, Windows), отчасти с тем, что Bash воспринимается скорее как средство автоматизации работы с файлами и утилитами, чем полноценный скриптовый язык, даже несмотря на наличие в арсенале sed и awk. Ещё одним минусом Bash является то, что при выполнении скрипта каждая запущенная с его помощью утилита создаёт свой процесс, что отражается на скорости выполнения и уровне использования ресурсов системы.  

**Python**


В отличие от Bash, Python является полноценным объектно-ориентированным языком программирования. Он входит в состав большинства распространенных дистрибутивов GNU/Linux, что позволяет использовать его в качестве альтернативной основы для написания скриптов, решающих задачи системного администрирования. Вот лишь несколько причин, по которым выбор нередко падает на Python:

*Удобочитаемость и компактность кода*

Благодаря соблюдению чётких синтаксических правил, скрипт, написанный на Python, будет понятен любому IT-специалисту, знакомому с программированием, даже если он видит этот код впервые. В то же время, при внесении изменений следует обращать внимание на правильную расстановку отступов – в Python они используются в качестве разграничителей блоков кода.

*Наличие (даже в стандартной комплектации) большого количества модулей, подключаемых с помощью оператора import*

Каждый из модулей состоит из набора функций и методов, которые поддерживают основные системные протоколы и форматы и легко используются при написании собственного кода. Таким образом, экономится время, а скрипт будет выглядеть более структурированным. Возможности Python также позволяют написать и подключить собственный модуль, если поставленная задача отличается специфичностью решения;

*Кроссплатформенность*

Скрипты Python работают и в среде Windows, и в MacOS, и в UNIX, включая FreeBSD и GNU/Linux. Этот язык широко используется и на мобильных платформах, таких как Symbian, Android. В этом преимущество Python. Bash такими возможностями не обладает и является «встроенным» инструментарием только для семейств _NIX, _BSD и GNU/Linux. Скрипт, однажды написанный на Python, с большой долей вероятности будет работать на разных платформах, решая схожие задачи, при условии, что код не будет содержать специфических для конкретной операционной системы функций.

Python является подходящим инструментарием для решения следующих задач администрирования:

– парсинг лога или конфигурационного файла с использованием регулярных выражений;

– разработка приложений, в том числе нестандартных, для работы с базами данных MySQL, Oracle, PostgreSQL, Sybase и др.;

– сбор и анализ статистики интернет-трафика с нескольких IP-адресов;

– преобразование данных в различные форматы, например, конвертация .ini-файлов в текст при помощи модуля ConfigParser;

– работа с файлами сервера при помощи FTP-клиента;

– поднятие простого прокси-сервера;

– мониторинг работоспособности сервиса, запущенного на сервере, с отправкой предупреждений на e-mail администратора в случае сбоя;

– поднятие ppp-соединения с использованием программы автодозвона;

– поиск дубликатов с запросом на удаление или перемещение в каталоге с большим количеством файлов;

– проверка целостности архивов бэкапа при помощи алгоритма md5;

Python – удобный инструмент для решения задач системного администрирования, как повседневных, так и более специфических. Он одинаково подходит для создания как скриптов, так и более сложных приложений, в особенности сетевых, а также может служить заменой стандартному shell в Linux. 




