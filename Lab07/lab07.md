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
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab07/Screenshot/17.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118135913-5c48da00-b425-11eb-854a-cc01e7676e8f.png))
 
*Рис 7.1. Удаление файла*

8.	В домашнем каталоге создала одной командой три новых каталога с именами letters, memos, misk. Затем удалила эти каталоги одной командой.: *(рис 8.1 и рис 8.2)*

```sudo mkdir letters memos misk```

 
 ![]()
 
*Рис 8.1. Создала три каталога*

```sudo rm -r letters memos misk```


![]()

*Рис 8.2. Удалила три каталога*


9.  Удалила ранее созданный каталог ```~/newdir``` командой ```rm```. Проверила, был ли каталог удалён.: *(рис 9.1)*

```sudo rm -r newdir```

```ls```
 
 ![]()
 
*Рис 9.1. Удалила каталог и проверила, был ли он удален*
 

10.	 С помощью командыman определила, какую опцию команды ```ls``` нужно использовать для просмотра содержимого не только указанного каталога, но и подката-
логов, входящих в него *(рис 10.1 и 10.2)*: 

```man ls```;

``` ls -a``` *(рис 10.3)*

![]()

![]()

*Рис 10.1 и 10.2. Команда man ls*

![]()

*Рис 10.3. Команда ld s -a*


11.	С помощью команды ```man``` определила набор опций команды ```ls```, позволяющий отсортировать по времени последнего изменения выводимый список содержимого
каталога с развёрнутым описанием файлов *(рис 11.1 и рис 11.2)*: 

```man ls```;

```ls -alF``` *(рис 11.3)*

![]()

![]()

*Рис 11.1 и 11.2. Команда man ls*

![]()

*Рис 11.3. Команда ls -alF*

12.	 Используя команду ```man``` для просмотра описания следующих команд: ```cd```, ```pwd```, ```mkdir```, ```rmdir```, ```rm```. Пояснила основные опции этих команд: 

 
 ```man cd```; *(рис 12.1)*
 
 Нет справочной страницы для команды cd.
 
 ![]()
 
 *Рис 12.1. Команда man cd*
 
 
 ```man pwd```; *(рис 12.2 и рис 12.3)*
 
 ![]()
 
 ![]()
 
 *Рис 12.4 и 12.5. Команда man pwd*
 
 
 ```man mkdir```; *(рис 12.6 и рис 12.7)*
 
 ![]()
 
 ![]()
 
 *Рис 12.6 и 12.7. Команда man mkdir*
 
 
 ```man rmdir```; *(рис 12.8 и рис 12.9 )*
 
 ![]()
 
 ![]()
 
 *Рис 12.8 и 12.9. Команда man rmdir*
 
 
 ```man rm```; *(рис 12.10 и 12.11)*
 
 ![]()
 
 ![]()
 
 *Рис 12.10 и 12.11. Команда man rm*


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



