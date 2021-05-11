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







# ***Анализ файловой системы Linux. Команды для работы с файлами и каталогами***

**Оглавление:**

1.	Введение:
  a) Цель работы
2.	Описание результатов выполнения задания;
3.	Вывод;
4.	Контрольные вопросы.

























# **Введение:**


*Команда для создания текстовых файлов.*

Для создания текстового файла удобно воспользоваться командой ```touch```.


*Команды просмотра текстовых файлов.*

Для просмотра небольших файлов удобно пользоваться командой ```cat```.


Для просмотра больших файлов используйте команду ```less``` — она позволяет осуществлять постраничный просмотр файлов (длина страницы соответствует размеру экрана).


Команда ```tail``` выводит несколько (по умолчанию 10) последних строк файла.


Копирование файлов и каталогов осуществляется при помощи команды ```cp```.


Команды ```mv``` и ```mvdir``` предназначены для перемещения и переименования файлов и каталагов.



# **Цель работы:**

Ознакомление с файловой системой Linux, её структурой, именами и содержанием каталогов. Приобретение практических навыков по применению команд для работы с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.



# **Описание результатов выполнения задания:**

1.  Выполнила все примеры, приведенные в описании лабораторной работы *(рис 1.1)*:

Один из примеров:

- ```cd```

  ```touch may```
  
  ```ls -l may```
  
  ```chmod u+x may```
  
  ```ls -l may```

   ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/1.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117856768-dbb39d80-b2ad-11eb-9085-46526574c062.png))
   
*Рис 1.1. Выполнение примеров*

2.	Скопировалала ```usr/include/``` в домашний каталог и назвала его ```equipment``` *(рис 2.1)*:

```cd /usr/include```

```sudo cp signal.h /home```

 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/2.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117856850-f0903100-b2ad-11eb-98e1-100e867ef4c4.png))
 
*Рис 2.1. Копирование и переименование*

3.	В домашнем каталоге создала директорию ```ski.plases```: *(рис 3.1)*

    ```sudo mkdir ski.plases```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/3.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117856986-1b7a8500-b2ae-11eb-82fe-2be7dede2545.png))
 
*Рис 3.1. Создание директории ```ski.plases```*

 
4.	Переместила файл ```equipment``` в каталог ```ski.plases``` *(рис 4.1)*: 

``` cd /home```

```sudo mv equipment ski.plases```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/4.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117857060-30efaf00-b2ae-11eb-993c-b5f0c5e6b6d8.png))

*Рис 4.1. Перемещение файла в каталог*

5.	Переименовала файл ```~/ski.plases/equipment``` в ```~/ski.plases/equiplist```: *(рис 5.1)*

```cd /home``` и ```ls```
 
 ![]()
 
*Рис 5.1. Переименовала файл*


6.	Создала в домашнем каталоге файл ```abc1``` и скопировала его в каталог ```~/ski.plases```, назвав его ```equiplist2```: *(рис 6.1, 6.2, 6.3)*

```sudo mkdir newdir```

 ![]()
 
*Рис 6.1. Создала файл*

 ![]()
 
*Рис 6.2. Скопировала его*

 ![]()
 
*Рис 6.3. Переименовала файл*

7.	Создала каталог с именем ```equipment```  в каталоге ```~/ski.plases```: *(рис 7.1)*

```cd newdir```;

```sudo mkdir morefun```
 
 ![]()
 
*Рис 7.1. Создание нового каталога в другом каталоге*

8.	Переместила файлы ```~/ski.plases/equiplist``` и ```equiplist2``` в каталог ```~/ski.plases/equipment```: *(рис 8.1)*

```sudo mkdir letters memos misk```

 
 ![]()
 
*Рис 8.1. Перемещение файлов*


9.  Создала и переместила каталог ```~/newdir``` в каталог ```~/ski.plases``` и назвала его ```plans```: *(рис 9.1, 9.2, 9.3)*

```sudo rm -r newdir```

```ls```
 
 ![]()
 
*Рис 9.1. Создание каталога*
 
 
 ![]()
 
*Рис 9.2. Перемещение в другой каталог*

 
 ![]()
 
*Рис 9.3. Переименование каталога*


10.	 Определила опции команды ```chmod```: 

-  ```drwxr--r--  ...  australia```

``` ls -a``` *(рис 10.3)*

![]()

*Рис 10.1 и 10.2. *


-  ```drwx--x--x. ...  play```


![]()

*Рис 10.1 и 10.2. *


-  ```-r-xr--r--  ...  my_os```


![]()

*Рис 10.3.*


-  ```-rw-rw-r--  ...  feathers```


![]()

*Рис 10.3.*


11.	Просмотрела содержимое файла ```/etc/xfce4``` *(рис 11.1)*: 

```cd /etc/xfce4```;


![]()

*Рис 11.1. Просмотр содержимого файла*


12.	 Скопировала файл ```~/feathers``` в файл ```~/file.old```: 

 
 ```man cd```; *(рис 12.1)*

 
 ![]()
 
 *Рис 12.1. Скопировала файл*
 
 
13.	Переместила файл ```~/file.old``` в каталог ```~/play```: *(рис 13.1)*
 
 ```history```
 
 ![]()
 
 
*Рис 13.1. Перемещение файла в каталог*

14. Скопировала каталог ```~/play``` в каталог ```~/fun``` *(рис 14.1)*:

![]()

*Рис 14.1. Копирование каталога в каталог*


15. Переместила каталог ```~/fun``` в каталог ```~/play``` и назвала его ```games``` *(рис 15.1)*:

![]()

*Рис 15.1. Перемещение каталога в каталог и переименование*


16. Лишила владельца файла ```~/feathers``` права на чтение *(рис 16.1)*:

![]()

*Рис 16.1. Лишение владельца права на чтение*


17. Ввела команду ```cat``` и попыталась просмотреть файл ```~/feathers```, на что система мне ответила, что у меня нет прав *(рис 17.1)*:

``` cat feathers```

![]()

*Рис 17.1. Попытка просмотра файла*

18. Дала владельцу файла ```~/feathers``` право на чтение *(рис 18.1)*:

![]()

*Рис 18.1. Получение права на чтение*


19. Лишила владельца каталога ```~/play``` права на выполнение *(рис 19.1)*:

![]()

*Рис 19.1. Лишение права на выполнение*

20. Попыталась перейти в каталог ```~/play```, на что система выдала ошибку, так как нет прав на выполнение у владельца *(рис 20.1)*:

![]()

*Рис 20.1. Попытка перейти в каталог без прав на выполнение*


21. Дала владельцу каталога ```~/play``` право на выполнение *(рис 18.1)*:

![]()

*Рис 18.1. Получение права на выполнение*


22. Использовала команду ```man``` для просмотра описания следующих команд: ```mount```, ```fsck```, ```mkfsr```, ```kill```. Кратко их охарактеризовала: 

 
 ```man mount```; *(рис 12.1 и рис 12.2)*
 
 ![]()
 
 ![]()
 
 *Рис 12.1 и 12.2. Команда man mount*
 
 
 ```man fsck```; *(рис 12.3 и рис 12.4)*
 
 ![]()
 
 ![]()
 
 *Рис 12.3 и 12.4. Команда man fsck*
 
 
 ```man mkfs```; *(рис 12.5 и рис 12.6 )*
 
 ![]()
 
 ![]()
 
 *Рис 12.5 и 12.6. Команда man mkfs*
 
 
 ```man kill```; *(рис 12.7 и 12.8)*
 
 ![]()
 
 ![]()
 
 *Рис 12.7 и 12.8. Команда man kill*




# **Вывод:**

В данной лабораторной работе, я ознакомилась с файловой системой Linux, её структурой, именами и содержанием каталогов. Приобрела практические навыки по применению команд для работы с файлами и каталогами, по управлению процессами (и работами), по проверке использования диска и обслуживанию файловой системы.



# **Контрольные вопросы (лабораторная работа №6)**

*1. Дайте характеристику каждой файловой системе, существующей на жёстком диске компьютера, на котором вы выполняли лабораторную работу.* 



*2.	Приведите общую структуру файловой системы и дайте характеристику каждой директории первого уровня этой структуры.*





*3. Какая операция должна быть выполнена, чтобы содержимое некоторой файловой системы было доступно операционной системе?*




*4.	Назовите основные причины нарушения целостности файловой системы. Как устранить повреждения файловой системы?* 



 
*5. Как создаётся файловая система?* 



*6.	Дайте характеристику командам, которые позволяют просмотреть текстовые файлы.* 




*7.	Приведите основные возможности команды ```cp``` в Linux.* 




*8.	Назовите и дайте характеристику командам перемещения и переименования файлов и каталогов.*




*9.	Что такое права доступа? Как они могут быть изменены?*

