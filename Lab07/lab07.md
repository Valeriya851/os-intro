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

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/15.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118135604-0d02a980-b425-11eb-988f-962cb4e2e1bf.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/16.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118135662-1be95c00-b425-11eb-86ef-bf8e2738eed7.png))

*Рис 6.2. Запуск в фоновом режиме процесса*

7.	Удалила файл ```logfile```: *(рис 7.1)*

```rm -r logfile```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/18.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118136743-41c33080-b426-11eb-9173-feae02117f55.png))
 
*Рис 7.1. Удаление файла*

8.	: *(рис 8.1)*

```gedit &```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/20.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137030-8d75da00-b426-11eb-93aa-26c6431b06bb.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/19.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118136885-68816700-b426-11eb-96c6-c1d4aee71d70.png))
 
*Рис 8.1. *


9.  : *(рис 9.1)*

```ps aux```

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/21.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137110-a67e8b00-b426-11eb-8c05-ad1f535678ce.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/22.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137288-db8add80-b426-11eb-9cdc-56995403df6e.png))
 
*Рис 9.1. *
 
```ps``` *(рис 9.2)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/23.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137499-1260f380-b427-11eb-9aef-1bc6d94312c3.png))

*Рис 9.2. *

```ps aux | grep gedit```*(рис 9.3)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/24.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137606-36243980-b427-11eb-9b0e-2a90f2892756.png))

*Рис 9.3. *

10.	 С помощью команды ```man``` определила опции команды ```kill```: 

```man kill``` *(рис 10.1)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/25.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137912-8f8c6880-b427-11eb-89cb-37abc65abaeb.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/26.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118137951-97e4a380-b427-11eb-8df4-ac8b0439b4aa.png))

*Рис 10.1. Команда man kill*

Завершила процесс с помощью команды ```kill```:

```kill %gedit```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/27.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118138128-c793ab80-b427-11eb-806c-5f97283955df.png))

*Рис 10.2. Завершение процесса с помощью команды ```kill```*


11.	С помощью команды ```man``` определила опции команды ```df```: 

```man df``` *(рис 11.1)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/28.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118138323-0164b200-b428-11eb-9e84-b26f7fecfea8.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/29.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118138438-23f6cb00-b428-11eb-858b-643a68403195.png))

*Рис 11.1. Команда man df*


12.	 Используя команду ```man``` для просмотра описания команды ```du```: 
 
 ```man du```; *(рис 12.1 и рис 12.2)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/30.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118138765-83ed7180-b428-11eb-9289-7ab05cdce7c7.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/31.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118138801-8cde4300-b428-11eb-8359-bfdea6208131.png))
 
 *Рис 12.1 и 12.2. Команда man du*
 

13.	Используя информацию, полученную при помощи команды history, выполнила модификацию и исполнение нескольких команд из буфера команд: *(рис 13.1 и рис 13.2, рис 13.3, рис 13.4)*
 
 ```history```
 
 ![]()
 
 ![]()
 
*Рис 13.1 и 13.2. История*


**Модификация**

```!1385:s/alF/F```

![]()

*Рис 13.3. Модификация*


**Исполнение нескольких команд из буфера команд**

```cd; ls; pwd```

![]()

*Рис 13.4. Исполнение нескольких команд из буфера команд*



# **Вывод:**

В данной лабораторной работе, я ознакомилась с инструментами поиска файлов и фильтрации текстовых данных. Приобрела практические навыки: по управлению процессами (и заданиями), по проверке использования диска и обслуживанию файловых систем.


# **Контрольные вопросы (лабораторная работа №7)**

*1. Какие потоки ввода вывода вы знаете?* 


*2.	Объясните разницу между операцией > и >>.*





*3.	Что такое конвейер?*




*4.	Что такое процесс? Чем это понятие отличается от программы?* 


 
*5. Что такое PID и GID?* 


*6.	Что такое задачи и какая команда позволяет ими управлять?* 


*7.	Найдите информацию об утилитах ```top``` и ```htop```. Каковы их функции?* 



*8.	Назовите и дайте характеристику команде поиска файлов. Приведите примеры использования этой команды.*




*9.	Можно ли по контексту (содержанию) найти файл? Если да, то как?*



*10. Как определить объем свободной памяти на жёстком диске?*


*11. Как определить объем вашего домашнего каталога?*



*12. Как удалить зависший процесс?*



