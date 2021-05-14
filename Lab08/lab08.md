---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №8"

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







# ***Командная оболочка Midnight Commander***

**Оглавление:**

1.	Введение:
  a) Цель работы
2.	Описание результатов выполнения задания;
3.	Вывод;
4.	Контрольные вопросы.

























**Введение:**




**Цель работы:**

Освоение основных возможностей командной оболочки Midnight Commander. Приобретение навыков практической работы по просмотру каталогов и файлов; манипуляций с ними.



**Описание результатов выполнения задания:**

1.  Изучила информацию о ```mc```, вызвав в командной строке ```man mc```*(рис 1.1 и 1.2)*:

```man mc```

   ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/1.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118288415-3b9c8500-b4f6-11eb-8561-b815604fa546.png))
   
   ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/2.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118288450-4820dd80-b4f6-11eb-9014-99a302474620.png))
   
*Рис 1.1 и 1.2. Изучение информации о команде ```mc```*

2.	 Запустила из командной строки ```mc```, изучила структуру и меню *(рис 2.1 и 2.2)*:

```mc```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/3.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118288981-b2d21900-b4f6-11eb-8747-dade4a40fa78.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/4.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118289891-a13d4100-b4f7-11eb-9d80-b071d42f38bc.png))
 
*Рис 2.1 и 2.2. Вызов ```mc```*

Меню пользователя *(рис 2.3)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/5.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118290041-cdf15880-b4f7-11eb-8d00-2f7b6e527318.png))

*Рис 2.3. Меню пользователя*


3.	Выполнила несколько операций в ```mc```, используя управляющие клавиши: *(рис 3.1)*

```F1``` Вызов контекстно-зависимой подсказки

```F2``` Вызов пользовательского меню с возможностью создания и/или дополнения дополнительных функций

```F3``` Просмотр содержимого файла, на который указывает подсветка в активной панели (без возможности редактирования)

```F4``` Вызов встроенного в mc редактора для изменения содержания файла, на который указывает подсветка в активной панели

```F5``` Копирование одного или нескольких файлов, отмеченных в первой (активной) панели, в каталог, отображаемый на второй панели

```F6``` Перенос одного или нескольких файлов, отмеченных в первой (активной) панели, в каталог, отображаемый на второй панели

```F7``` Создание подкаталога в каталоге, отображаемом в активной панели

```F8``` Удаление одного или нескольких файлов (каталогов), отмеченных в первой (активной) панели файлов

```F9``` Вызов меню mc

```F10``` Выход из mc
 
 
4.  Выполнила основные команды меню левой панели *(рис 4.1)*: `

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/8.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118291348-51f81000-b4f9-11eb-8e17-4d5c3c853dc3.png))

*Рис 4.1. Левая панель*

Информация о файле *(рис 4.2)*:

  ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/9.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118291531-866bcc00-b4f9-11eb-9bf7-fba74b628804.png))
  
 *Рис 4.2. Информация*
 
 Дерево каталогов *(рис 4.3)*:
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/10.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118291783-c9c63a80-b4f9-11eb-9947-f03ab27e6725.png))
 
 *Рис 4.3. Дерево каталогов*
 
 Формат списка файлов *(рис 4.4)*:
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/11.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118292030-085bf500-b4fa-11eb-95f5-464bf4807b4b.png))
 
 *Рис 4.4. Формат списка файлов*
 
 
5.	Использовала возможности подменю ```Файл```: *(рис 5.1)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/12.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118292451-730d3080-b4fa-11eb-95b6-30e8ad5dadd5.png))
 
*Рис 5.1. Подменю ```Файл```*

- Просмотрела содержимое текстового файла *(рис 5.2 и 5.3)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/13.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118292616-a354cf00-b4fa-11eb-8724-747f100f7ed3.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/14.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118292684-b5367200-b4fa-11eb-8643-9a9227402a12.png))

*Рис 5.2 и 5.3. Просмотр содержимого текстового файла*

- Отредактировала содержимое текстового файла, добавила hello и hi *(рис 5.4 и 5.5)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/15.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118293169-31c95080-b4fb-11eb-84ac-6994ebab8381.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/17.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118293215-3f7ed600-b4fb-11eb-8334-8a069716fef5.png))

*Рис 5.4 и 5.5. Правка содержимого файла*

- Создала каталог hello *(рис 5.6 и 5.7)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/18.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118293523-8d93d980-b4fb-11eb-94b2-4e03edd48eb7.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/19.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118293733-c764e000-b4fb-11eb-99e6-72555da7e7d6.png))

*Рис 5.6 и 5.7. Создание каталога*

- Скопировала файл в созданный каталог *(рис 5.8 и 5.9)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/20.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118293956-085cf480-b4fc-11eb-99e3-89ce63460550.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/21.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118294018-19a60100-b4fc-11eb-9d58-64cbbf76b4a5.png))

*Рис 5.8 и 5.9. Копирование файлов в каталог*


6.	С помощью соответствующих средств подменю ```Команда``` выполнила задания *(рис 6.1)*:

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/22.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118295153-59211d00-b4fd-11eb-9d71-ff2c9c5e0ff1.png))
 
*Рис 6.1. Подменю ```Команда```*

- Нашла в файловой системе файл с заданными условиями (с расширением .cpp + строка main) *(рис 6.2 и 6.3)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/23.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118295683-f9774180-b4fd-11eb-957e-74092db3b31b.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/24.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118295772-0a27b780-b4fe-11eb-9230-8cc9bd0f8f7c.png))

*Рис 6.2 и 6.3. Нахождение файла с заданными условиями*

- История операций + выбор одной из них *(рис 6.4)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/25.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118296107-67bc0400-b4fe-11eb-9401-65b4df73e3af.png))

*Рис 6.4. История*

- Перешла в домашний каталог *(рис 6.5 и 6.6)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/26.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118296327-a6ea5500-b4fe-11eb-9b5c-baaba10b02b4.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/27.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118296389-b9fd2500-b4fe-11eb-8c5f-43cb0b683372.png))

*Рис 6.5 и 6.6. Переход в домашний каталог*

- Анализ файла ```profile``` и файла ```bash``` *(рис 6.7)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/28.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118296653-08122880-b4ff-11eb-8ff2-e5842313d71b.png))

*Рис 6.7. Сравнение*

7.	В каталоге ```~/newdir``` создайте новый каталог с именем ```morefun```: *(рис 7.1)*

```cd newdir```;

```sudo mkdir morefun```
 
 ![]()
 
*Рис 7.1. Создание нового каталога*

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



**Вывод:**

В данной лабораторной работе, я освоила основные возможности командной оболочки Midnight Commander. Приобрела навыкы практической работы по просмотру каталогов и файлов; манипуляций с ними.



# **Контрольные вопросы (лабораторная работа №8)**

*1. Какие режимы работы есть в mc. Охарактеризуйте их.* 




*2.	Какие операции с файлами можно выполнить как с помощью команд shell, так и с помощью меню (комбинаций клавиш) mc? Приведите несколько примеров.*




*3.	Опишите структура меню левой (или правой) панели mc, дайте характеристику командам.*



*4.	Опишите структура меню ```Файл``` mc, дайте характеристику командам.* 



 
*5. Опишите структура меню ```Команда```mc, дайте характеристику командам.* 




*6.	Опишите структура меню ```Настройки``` mc, дайте характеристику командам.* 




*7.	Назовите и дайте характеристику встроенным командам mc.* 




*8.	Назовите и дайте характеристику командам встроенного редактора mc.*




*9.	Дайте характеристику средствам mc, которые позволяют создавать меню, определяемые пользователем.*




*10. Дайте характеристику средствам mc, которые позволяют выполнять действия, определяемые пользователем, над текущим файлом.*
