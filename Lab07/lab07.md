---
# Front matter
lang: ru-RU
title: "Отчет по второй лабораторной работе №6"

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







# ***Поиск файлов. Перенаправление ввода-вывода. Просмотр запущенных процессов***

**Оглавление:**

1.	Введение:
  a) Цель работы
2.	Описание результатов выполнения задания;
3.	Вывод;
4.	Контрольные вопросы.

























# **Введение:**

В системе по умолчанию открыто три специальных потока:

– stdin — стандартный поток ввода (по умолчанию: клавиатура), файловый де-
скриптор 0;

– stdout — стандартный поток вывода (по умолчанию: консоль), файловый де-
скриптор 1;

– stderr — стандартный поток вывод сообщений об ошибках (по умолчанию:
консоль), файловый дескриптор 2.

*Конвейер (pipe)* служит для объединения простых команд или утилит в цепочки, в которых результат работы предыдущей команды передаётся последующей.

Команда ```find``` используется для поиска и отображения имён файлов, соответ- ствующих заданной строке символов.

Найти в текстовом файле указанную строку символов позволяет команда ```grep```.

Команда ```df``` показывает размер каждого смонтированного раздела диска.

Команда ```du``` показывает число килобайт, используемое каждым файлом или каталогом.

Любой команде, выполняемой в системе, присваивается идентификатор процесса (process ID). Получить информацию о процессе и управлять им, пользуясь идентификатором процесса, можно из любого окна командного интерпретатора.

Команда ```ps``` используется для получения информации о процессах.


# **Цель работы:**

Ознакомление с инструментами поиска файлов и фильтрации текстовых данных. Приобретение практических навыков: по управлению процессами (и заданиями), по проверке использования диска и обслуживанию файловых систем.


# **Описание результатов выполнения задания:**

1.  Записала в файл ```file.txt``` названия файлов, содержащихся в каталоге ```/etc``` *(рис 1.1)*:

```cat >> file.txt```

   ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/1.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118131574-851aa080-b420-11eb-814d-57d7a4e75e13.png))
   
   ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/2.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118131716-ae3b3100-b420-11eb-986f-3ef8f87ef6b5.png))
   
 *Рис 1.1. Запись файлов из каталога ```/etc``` в файл*
 
 Дописала в файл названия файлов, содержащихся в домашнем каталоге:
 
 ```cat >> file.txt```
 
   ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/3.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118131749-bb582000-b420-11eb-8313-441d446eb0b7.png))
   
*Рис 1.2. Добавление в файл ```file.txt``` файлов из домашнего каталога*

2.	 Вывела имена всех файлов из ```file.txt```, имеющих расширение ```.conf```*(рис 2.1)*:

```grep .conf file.txt```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/4.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118132085-1d188a00-b421-11eb-8432-16e1afbac34e.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/5.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118132136-2d306980-b421-11eb-87dd-c02a4329c93d.png))
 
*Рис 2.1. Вывод всех файлов имеющих расширение ```.conf```*

3.	Записала выведенные имена в новый текстовый файл ```conf.txt```:

Создала текстовый файл: *(рис 3.1)*

```touch conf.txt```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/6.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118132532-9c0dc280-b421-11eb-8ba2-46f197271ba2.png))
 
*Рис 3.1. Создание текстового файла*

Добавила имена файлов в новый файл: *(рис 3.2)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/7.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118132914-09215800-b422-11eb-94cf-fc70068c40ea.png))
 
*Рис 3.2. Добавление в файл*

 
 
4.	Определила, какие файлы в моем домашнем каталоге имеют имена, начинающиеся с символа **c**: 

Первый вариант: 

```find ~ -name "c*" -print``` *(рис 4.1)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/8.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118133733-fc513400-b422-11eb-9fdc-1077483b5dbf.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/9.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118133813-13902180-b423-11eb-9a16-76e7070a97df.png))

*Рис 4.1. Нахождение файлов начинающихся с **c** *

Второй вариант: 

```ls -l | grep c*``` *(рис 4.2)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/10.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118134099-5d790780-b423-11eb-87f7-32c65f567970.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/11.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118134420-b8aafa00-b423-11eb-8055-44d722f36949.png))

*Рис 4.2. Нахождение файлов начинающихся с **c** *


5.	Вывела на экран (постранично) имена файлов из каталога ```/etc```, начинающихся с символа ```h```: *(рис 5.1)*

Перешла в каталог ```/etc```:

``` cd /etc```

```ls -l h* |less```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/12.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118134653-fdcf2c00-b423-11eb-9a62-02fc4c340044.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/13.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118134821-2820e980-b424-11eb-8d50-de80699b2c99.png))
 
*Рис 5.1. Вывод на экран имен файлов из каталога ```/etc```, начиняющихся с символа ```h```*


6.	Создала файл ```logfile``` и запустила в фоновом режиме процесс, который записал в новый файл имена, которые начинаются с ```log```: 

```touch logfile``` *(рис 6.1)*

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/14.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118135345-b8f7c500-b424-11eb-8fd7-5bd3afa1d1ac.png))
 
*Рис 6.1. Создание файла*

Запустила в фоновом режиме процесс, который  добавил в файл ```logfile``` имена которые начинаются с ```log```: *(рис 6.2)*

```find ~ -name "log*" -print > logfile &```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/15.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118135604-0d02a980-b425-11eb-988f-962cb4e2e1bf.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/16.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118135662-1be95c00-b425-11eb-86ef-bf8e2738eed7.png))

*Рис 6.2. Запуск в фоновом режиме процесса*

7.	Удалила файл ```logfile```: *(рис 7.1)*

```rm -r logfile```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/18.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118136743-41c33080-b426-11eb-9173-feae02117f55.png))
 
*Рис 7.1. Удаление файла*

8.	Запустила в фоновом режиме редактор ```gedit```: *(рис 8.1 и 8.2)*

```gedit &```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/20.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137030-8d75da00-b426-11eb-93aa-26c6431b06bb.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/19.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118136885-68816700-b426-11eb-96c6-c1d4aee71d70.png))
 
*Рис 8.1 и 8.2. Запуск редактора в фоновом режиме*


9.  Определила идентификатор процесса ```gedit```, мспользуя команду ```ps``` и фильтр ```grep```:

Для получения информации о процессах, управляемых вами и запущенных (работающих или остановленных) на вашем терминале, используйте опцию ```aux```.

```ps aux```  *(рис 9.1 и 9.2)*

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/21.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137110-a67e8b00-b426-11eb-8c05-ad1f535678ce.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/22.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137288-db8add80-b426-11eb-9cdc-56995403df6e.png))
 
*Рис 9.1 и 9.2. Получение информации о процессах, управляемых вами и запущенных на вашем терминале*
 
 Команда ```ps``` используется для получения информации о процессах.
 
```ps``` *(рис 9.2)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/23.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137499-1260f380-b427-11eb-9aef-1bc6d94312c3.png))

*Рис 9.2. Получение информации о процессах*

Фильтр ```grep```:

```ps aux | grep gedit```*(рис 9.3)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/24.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137606-36243980-b427-11eb-9b0e-2a90f2892756.png))

*Рис 9.3. Фильтр ```grep```*

10.	 С помощью команды ```man``` определила опции команды ```kill```: 

```man kill``` *(рис 10.1)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/25.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137912-8f8c6880-b427-11eb-89cb-37abc65abaeb.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/26.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137951-97e4a380-b427-11eb-8df4-ac8b0439b4aa.png))

*Рис 10.1. Команда man kill*

Завершила процесс ```gedit``` с помощью команды ```kill```:

```kill %gedit```  *(рис 10.2)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/27.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118138128-c793ab80-b427-11eb-806c-5f97283955df.png))

*Рис 10.2. Завершение процесса с помощью команды ```kill```*


11.	С помощью команды ```man``` определила опции команды ```df```: 

```man df``` *(рис 11.1 и 11.2)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/28.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118138323-0164b200-b428-11eb-9e84-b26f7fecfea8.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/29.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118138438-23f6cb00-b428-11eb-858b-643a68403195.png))

*Рис 11.1 и 11.2. Команда man df*


12.	 Используя команду ```man``` для просмотра описания команды ```du```: 
 
 ```man du```; *(рис 12.1 и рис 12.2)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/30.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118138765-83ed7180-b428-11eb-9289-7ab05cdce7c7.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/31.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118138801-8cde4300-b428-11eb-8359-bfdea6208131.png))
 
 *Рис 12.1 и 12.2. Команда man du*
 

13.	Выполнила команды ```df``` и ```du```: 

Команда ```df``` показывает размер каждого смонтированного раздела диска.
 
 ```df -vi``` *(рис 13.1 и 13.2)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/32.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118139018-c6af4980-b428-11eb-894f-313a142fbd6a.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/33.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118139077-d3cc3880-b428-11eb-9c52-e0e781a9ccc2.png))
 
*Рис 13.1 и 13.2. Размер каждого смонтированного раздела диска*

Команда ```du``` показывает число килобайт, используемое каждым файлом или каталогом.

```du -a ~/```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/34.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118139206-f3636100-b428-11eb-8aca-503283d19755.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/35.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118139262-ffe7b980-b428-11eb-9ff6-c97524ae64de.png))

*Рис 13.3 и 13.4. Число килобайт, используемое домашним каталогом*

14. С помощью команды ```man``` определила опции команды ```find```: 

```man find``` *(рис 14.1 и 14.2)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/36.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118139558-4b01cc80-b429-11eb-86ff-6a5c78c5b4fd.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/37.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118139589-535a0780-b429-11eb-87ff-5f8f956a89bd.png))

*Рис 14.1 и 14.2. Команда man find*

15. С помощью команды ```man find``` определила операцию, которая выводит имена всех директорий, имеющихся в домашнем каталоге:

```-type``` - тип искомого, ```d``` - каталог;

```find -type d -print``` *(рис 15.1 и 15.2)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/38.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118139896-a469fb80-b429-11eb-8afb-25709ed1b30f.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/39.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118139938-b0ee5400-b429-11eb-9629-1d9e60479581.png))

*Рис 15.1 и 15.2. Вывод имен всех директорий, имеющихся в домашнем каталоге*


# **Вывод:**

В данной лабораторной работе, я ознакомилась с инструментами поиска файлов и фильтрации текстовых данных. Приобрела практические навыки: по управлению процессами (и заданиями), по проверке использования диска и обслуживанию файловых систем.


# **Контрольные вопросы (лабораторная работа №7)**

*1. Какие потоки ввода вывода вы знаете?* 

В системе по умолчанию открыто три специальных потока:

– stdin — стандартный поток ввода (по умолчанию: клавиатура), файловый де-
скриптор 0;

– stdout — стандартный поток вывода (по умолчанию: консоль), файловый де-
скриптор 1;

– stderr — стандартный поток вывод сообщений об ошибках (по умолчанию:
консоль), файловый дескриптор 2.


*2.	Объясните разницу между операцией > и >>.*

#Создаёт файл, содержащий список дерева каталогов.

```ls -lR > dir-tree.list```

```1>filename```

#Перенаправление вывода (stdout) в файл "filename". 

```1>>filename```

#Перенаправление вывода (stdout) в файл "filename", 

#файл открывается в режиме добавления.

```2>filename```

#Перенаправление stderr в файл "filename". 

```2>>filename```

#Перенаправление stderr в файл "filename",

#файл открывается в режиме добавления.

```&>filename```

#Перенаправление stdout и stderr в файл "filename".



*3.	Что такое конвейер?*

**Конвейер** в терминологии операционных систем семейства Unix — некоторое множество процессов, для которых выполнено следующее перенаправление ввода-вывода: то, что выводит на поток стандартного вывода предыдущий процесс, попадает в поток стандартного ввода следующего процесса.

**Конвейер (pipe)** служит для объединения простых команд или утилит в цепочки, в которых результат работы предыдущей команды передаётся последующей.


*4.	Что такое процесс? Чем это понятие отличается от программы?* 

Термин *процесс* впервые появился при разработке операционной системы Multix и имеет несколько определений, которые используются в зависимости от контекста. Процесс - это: программа на стадии выполнения "объект", которому выделено процессорное время

Любой команде, выполняемой в системе, присваивается идентификатор процесса (process ID). Получить информацию о процессе и управлять им, пользуясь идентификатором процесса, можно из любого окна командного интерпретатора.

Компьютерная программа сама по себе — лишь пассивная последовательность инструкций. В то время как процесс — непосредственное выполнение этих инструкций. Также, процессом называют выполняющуюся программу и все её элементы: адресное пространство, глобальные переменные, регистры, стек, открытые файлы и так далее.
 
 
*5. Что такое PID и GID?* 

**Идентификатор процесса (англ. Process IDentifier, PID)** — уникальный номер (идентификатор) процесса в многозадачной операционной системе (ОС). Например, в ОС Linux PID хранится в переменной целочисленного типа (int).

***Идентификатор группы (GID)***

Группы пользователей применяются для организации доступа нескольких пользователей к некоторым ресурсам. У группы, так же, как и у пользователя, есть имя и идентификационный номер — **GID (Group ID)**.


*6.	Что такое задачи и какая команда позволяет ими управлять?* 

Любую выполняющуюся в консоли команду или внешнюю программу можно запустить в фоновом режиме. Для этого следует в конце имени команды указать знак амперсанда ```&. ```

Например:

```gedit &```

Будет запущен текстовой редактор gedit в фоновом режиме. Консоль при этом не будет заблокирована.

Запущенные фоном программы называются задачами (jobs). Ими можно управлять с помощью команды jobs, которая выводит список запущенных в данный момент задач. 

Для завершения задачи необходимо выполнить команду

```kill %номер задачи```


*7.	Найдите информацию об утилитах ```top``` и ```htop```. Каковы их функции?* 

```top``` (table of processes) — консольная команда, которая выводит список работающих в системе процессов и информацию о них. По умолчанию она в реальном времени сортирует их по нагрузке на процессор. Программа написана для UNIX-совместимых операционных систем и опубликована под свободной лицензией GNU FDL.

```htop``` — продвинутый монитор процессов, написанный для Linux. Он был задуман заменить стандартную программу top. ... В отличие от top, htop показывает все процессы в системе. Также показывает время непрерывной работы, использование процессоров и памяти.


*8.	Назовите и дайте характеристику команде поиска файлов. Приведите примеры использования этой команды.*

Команда ```find``` используется для поиска и отображения имён файлов, соответствующих заданной строке символов.

Формат команды:

```find путь [-опции]```

Путь определяет каталог, начиная с которого по всем подкаталогам будет вестись поиск.

Примеры:

1. Вывести на экран имена файлов из вашего домашнего каталога и его подкаталогов, начинающихся на f:

```find ~ -name "f*" -print```,

где ```~``` — обозначение вашего домашнего каталога, ```-name``` — после этой опции указывается имя файла, который нужно найти, ```"f*"``` — строка символов, опре- деляющая имя файла, -print — опция, задающая вывод результатов поиска на экран.

2. Вывести на экран имена файлов в каталоге ```/etc```, начинающихся с символа p: 

```find /etc -name "p*" -print```


*9.	Можно ли по контексту (содержанию) найти файл? Если да, то как?*

**Фильтрация текста**

Найти в текстовом файле указанную строку символов позволяет команда ```grep```.

Формат команды:

```grep строка имя_файла```

Кроме того, команда grep способна обрабатывать стандартный вывод другихк оманд (любой текст). Для этого следует использовать конвейер, связав вывод команды с вводом ```grep```.

Примеры:

1. Показать строки во всех файлах в вашем домашнем каталоге с именами, начинающимися на f, в которых есть слово begin:

```grep begin f*```

2. Найти в текущем каталоге все файлы, в имени которых есть буквосочетание «лаб»:

  ```ls -l | grep лаб```


*10. Как определить объем свободной памяти на жёстком диске?*

Команда ```df``` показывает размер каждого смонтированного раздела диска.

Формат команды:

```df [-опции] [файловая_система]```

Пример:

```df -vi```


*11. Как определить объем вашего домашнего каталога?*

Команда ```du``` показывает число килобайт, используемое каждым файлом или каталогом.

Формат команды:

```du [-опции] [имя_файла...]```

Пример.

```du -a ~/```

На ```afs``` можно посмотреть использованное пространство командой

```fs quota```


*12. Как удалить зависший процесс?*

Находим PID зависшего процесса;

«Убиваем» процесс командой ```kill```:

Когда известен PID процесса, мы можем убить его командой ```kill```. Команда ```kill``` принимает в качестве параметра PID процесса. 

Убиваем процессы командой ```killall```:

Команда ```killall``` в Linux предназначена для «убийства» всех процессов, имеющих одно и то же имя. Это удобно, так как нам не нужно знать PID процесса. 
