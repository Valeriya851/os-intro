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

```sudo mv equipment equiplist``` 
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/5.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117857897-179b3280-b2af-11eb-96b8-6d2764a9b711.png))
 
*Рис 5.1. Переименовала файл*


6.	Создала в домашнем каталоге файл ```abc1``` и скопировала его в каталог ```~/ski.plases```, назвав его ```equiplist2```: *(рис 6.1, 6.2, 6.3)*

```sudo touch abc1```

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/6.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117857987-3699c480-b2af-11eb-945a-422f3ad06546.png))
 
*Рис 6.1. Создала файл*


```sudo cp abc1 ski.plases```


 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/7.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117858045-474a3a80-b2af-11eb-93e9-8659454861eb.png))
 
*Рис 6.2. Скопировала его*

```cd ski.plases```

```sudo mv abc1 equiplist2```


 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/8.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117858168-6b0d8080-b2af-11eb-9f55-e43045d62156.png))
 
*Рис 6.3. Переименовала файл*

7.	Создала каталог с именем ```equipment```  в каталоге ```~/ski.plases```: *(рис 7.1)*

```sudo mkdir equipment```
 
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/9.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117858309-942e1100-b2af-11eb-8d63-7ae7e63218a8.png))
 
*Рис 7.1. Создание нового каталога в другом каталоге*

8.	Переместила файлы ```~/ski.plases/equiplist``` и ```equiplist2``` в каталог ```~/ski.plases/equipment```: *(рис 8.1)*

```sudo mv equiplist equiplist2 equipment```

 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/10.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117860186-d35d6180-b2b1-11eb-8027-0e68468ff45e.png))
 
*Рис 8.1. Перемещение файлов*


9.  Создала и переместила каталог ```~/newdir``` в каталог ```~/ski.plases``` и назвала его ```plans```: *(рис 9.1, 9.2, 9.3)*

```cd /home```

```sudo mkdir newdir```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/11.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117860305-f5ef7a80-b2b1-11eb-8d24-732d2900f34e.png))
 
*Рис 9.1. Создание каталога*
 
 ```sudo mv newdir ski.plases```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/12.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117860391-10c1ef00-b2b2-11eb-9e30-886687ec1341.png))
 
*Рис 9.2. Перемещение в другой каталог*

```cd ski.plases```

```sudo mv newdir plans```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/13.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117860500-2d5e2700-b2b2-11eb-8ea6-ab0d99669e37.png))
 
*Рис 9.3. Переименование каталога*


10.	 Определила опции команды ```chmod```: 

-  ```drwxr--r--  ...  australia```

```sudo touch australia``` *(рис 10.1)*

```sudo chmod 744 australia```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/14.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117860601-4bc42280-b2b2-11eb-876a-5f40d1fa4672.png))

*Рис 10.1. Определение опции команды ```chmod```*


-  ```drwx--x--x. ...  play``` *(рис 10.2)*

```sudo touch play```

```sudo chmod 711 play```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/15.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117860835-9180eb00-b2b2-11eb-88e3-bc35c1cc581b.png))

*Рис 10.2. Определение опции команды ```chmod```*


-  ```-r-xr--r--  ...  my_os``` *(рис 10.3)*

```sudo touch my_os```

```sudo chmod 154 my_os```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/16.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117861089-dc9afe00-b2b2-11eb-9ded-d792948a7a4c.png))

*Рис 10.3. Определение опции команды ```chmod```*


-  ```-rw-rw-r--  ...  feathers``` *(рис 10.4)*

```sudo touch feathers```

```sudo chmod 664 feathers```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/17.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117861208-fdfbea00-b2b2-11eb-97bd-db1053d792ab.png))

*Рис 10.4. Определение опции команды ```chmod```*


11.	Просмотрела содержимое файла ```/etc/xfce4``` *(рис 11.1)*: 

```cd /etc/xfce4```

```ls```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/18.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117861371-2d125b80-b2b3-11eb-9c41-0ac9215fd2bd.png))

*Рис 11.1. Просмотр содержимого файла*


12.	 Скопировала файл ```~/feathers``` в файл ```~/file.old```: 

 
 ```sudo touch file.old```; *(рис 12.1)*

 ```sudo cp feathers file.old```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/19.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117861459-46b3a300-b2b3-11eb-86b4-e4b77b5ad2d9.png))
 
 *Рис 12.1. Скопировала файл*
 
 
13.	Переместила файл ```~/file.old``` в каталог ```~/play```: *(рис 13.1)*
 
 ```sudo mv feathers play```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/20.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117861601-69de5280-b2b3-11eb-91cf-eaf85db16d07.png))
 
 
*Рис 13.1. Перемещение файла в каталог*

14. Скопировала каталог ```~/play``` в каталог ```~/fun``` *(рис 14.1)*:

```sudo mkdir fun```

```sudo cp -r play fun```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/21.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117861692-88dce480-b2b3-11eb-9dd7-a3713471219b.png))

*Рис 14.1. Копирование каталога в каталог*


15. Переместила каталог ```~/fun``` в каталог ```~/play``` и назвала его ```games``` *(рис 15.1)*:

```sudo mv fun play```

```ls play```

```cd play```

```sudo mv fun games```

```ls```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/22.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117861819-b1fd7500-b2b3-11eb-8d47-503cbede5101.png))

*Рис 15.1. Перемещение каталога в каталог и переименование*


16. Лишила владельца файла ```~/feathers``` права на чтение *(рис 16.1)*:

```sudo chmod -r feathers```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/25.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117862047-ff79e200-b2b3-11eb-9d45-c8f490e65a76.png))

*Рис 16.1. Лишение владельца права на чтение*


17. Ввела команду ```cat``` и попыталась просмотреть файл ```~/feathers```, на что система мне ответила, что у меня нет прав *(рис 17.1)*:

``` cat feathers```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/23.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117861967-e3764080-b2b3-11eb-82be-6475f492b98d.png))

*Рис 17.1. Попытка просмотра файла*

18. Дала владельцу файла ```~/feathers``` право на чтение *(рис 18.1)*:


```sudo chmod +r feathers```


19. Лишила владельца каталога ```~/play``` права на выполнение *(рис 19.1)*:

```sudo chmod -x play```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/26.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117862107-1a4c5680-b2b4-11eb-935d-a26bfa5fabfb.png))

*Рис 19.1. Лишение права на выполнение*

20. Попыталась перейти в каталог ```~/play```, на что система выдала ошибку, так как нет прав на выполнение у владельца *(рис 20.1)*:

```cd play```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/27.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117862172-2cc69000-b2b4-11eb-9da9-7dc0b40d0e42.png))

*Рис 20.1. Попытка перейти в каталог без прав на выполнение*


21. Дала владельцу каталога ```~/play``` право на выполнение *(рис 18.1)*:

```sudo chmod +x play```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/28.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117862230-3ea83300-b2b4-11eb-9832-2c1e24217f08.png))

*Рис 18.1. Получение права на выполнение*


22. Использовала команду ```man``` для просмотра описания следующих команд: ```mount```, ```fsck```, ```mkfsr```, ```kill```. Кратко их охарактеризовала: 

 
 ```man mount```; *(рис 12.1 и рис 12.2)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/29.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117862317-57b0e400-b2b4-11eb-9e0b-6815dae99a32.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/30.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117862341-60091f00-b2b4-11eb-996f-6840b015bcff.png))
 
 *Рис 12.1 и 12.2. Команда man mount*
 
 
 ```man fsck```; *(рис 12.3 и рис 12.4)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/31.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117862387-6a2b1d80-b2b4-11eb-96fa-8c0e232faed9.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/32.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117862416-71522b80-b2b4-11eb-970f-6aac9b3099c8.png))
 
 *Рис 12.3 и 12.4. Команда man fsck*
 
 
 ```man mkfs```; *(рис 12.5 и рис 12.6 )*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/33.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117862447-79aa6680-b2b4-11eb-9b7f-9e312919eb0f.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/34.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117862482-8333ce80-b2b4-11eb-9f7c-6850f1ff684b.png))
 
 *Рис 12.5 и 12.6. Команда man mkfs*
 
 
 ```man kill```; *(рис 12.7 и 12.8)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/35.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117862524-8b8c0980-b2b4-11eb-8b08-56a9a49fc2e2.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab06/Screenshot/36.png?raw=true![image](https://user-images.githubusercontent.com/83212205/117862550-95157180-b2b4-11eb-90ba-e958c3ecea8e.png))
 
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

