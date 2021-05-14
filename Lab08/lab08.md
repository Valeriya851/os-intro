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

# **Оглавление:**

1.	Введение:
  a) Цель работы
2.	Описание результатов выполнения задания;
3.	Вывод;
4.	Контрольные вопросы.

























# **Введение:**

*Командная оболочка* — интерфейс взаимодействия пользователя с операционной системой и программным обеспечением посредством команд.

*Midnight Commander (или mc)* — псевдографическая командная оболочка для UNIX/Linux систем. Для запуска mc необходимо в командной строке набрать mc и
нажать Enter .

Рабочее пространство mc имеет две панели, отображающие по умолчанию списки файлов двух каталогов


# **Цель работы:**

Освоение основных возможностей командной оболочки Midnight Commander. Приобретение навыков практической работы по просмотру каталогов и файлов; манипуляций с ними.



# **Описание результатов выполнения задания:**

# Задание по mc

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

7.	Вызвала подменю ```Настройки```: *(рис 7.1)*

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/29.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118297001-6a6b2900-b4ff-11eb-9e9c-d0cba1315c9e.png))
 
*Рис 7.1. Подменю ```Настройки```*

- Параметры конфигурации *(рис 7.2)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/30.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118297200-a7cfb680-b4ff-11eb-8095-455fb5048132.png))

*Рис 7.2. Параметры конфигурации*

- Внешний вид *(рис 7.3)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/31.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118297407-e7969e00-b4ff-11eb-96d1-b914272d9c59.png))

*Рис 7.3. Внешний вид*

- Настройки панели *(рис 7.4)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/32.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118297537-1e6cb400-b500-11eb-8ee4-b34b23cab3b8.png))

*Рис 7.4. Настройки панели*

- Оформление *(рис 7.5)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/33.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118297729-5f64c880-b500-11eb-82da-17776751da0a.png))

*Рис 7.5. Оформление*

- Настройки виртуальной файловой системы *(рис 7.6)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/34.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118297916-976c0b80-b500-11eb-8b21-8f19b14d8046.png))

*Рис 7.6. Настройки виртуальной файловой системы*



# Задание по встроенному редактору mc

8.	Создала новый текстовый файл ```file1.txt```:

```touch file1.txt```


9.  Открыла этот файл с помощью встроенного в mc редактора: 

```F4```
 

10.	 Вставила в текстовый файл фрагмент текста про львов и выполнила с ним следующие задания:


**Клавиши для редактирования файла**

```Ctrl-y``` удалить строку

```Ctrl-u``` отмена последней операции

```Ins``` вставка/замена

```F7``` поиск (можно использовать регулярные выражения)

```^-F7``` повтор последней операции поиска

```F4``` замена

```F3``` первое нажатие — начало выделения, второе — окончание выделения

```F5``` копировать выделенный фрагмент

```F6``` переместить выделенный фрагмент

```F8``` удалить выделенный фрагмент

```F2``` записать изменения в файл

```F10``` выйти из редактора


Выполнила с текстовым файлом следующие действия *(рис 10.1)*:

- Удалила строку текста.

- Выделила фрагмент текста и скопируйте его на новую строку.

- Выделила фрагмент текста и перенесите его на новую строку.

- Сохранила файл.

- Отменила последнее действие.

- Перешла в конец файла (нажав комбинацию клавиш) и написала некоторый текст *(рис 10.2)*.

- Перешла в начало файла (нажав комбинацию клавиш) и написала некоторый текст *(рис 10.3)*.

- Сохранила и закроыла файл *(рис 10.4 и 10.5, 10.6)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/35.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118300304-99839980-b503-11eb-8611-48cb44ad06ae.png))

*Рис 10.1. Итог работы с текстовым файлом*


![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/36.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118300423-b8822b80-b503-11eb-92fd-c91f1b1b83ff.png))

*Рис 10.2. Переход в конец файла и добавление текста*


![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/37.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118300594-ee271480-b503-11eb-9b46-7c2ecd86791c.png))

*Рис 10.3. Переход в начало файла и добавление текста*

Сохранение и завершение файла:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/38.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118300744-19116880-b504-11eb-9d17-a3a1847b8be7.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/39.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118300941-4e1dbb00-b504-11eb-99fd-01109f43e259.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab08/Screenshot/40.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118300998-6261b800-b504-11eb-9379-e8419f30cccd.png))

*Рис 10.4. 10.5, 10.6. Сохранение и завершение*

11.	Открыла файл с исходным текстом на языке С и используя меню редактора включила подстветку синтаксиса.



**Вывод:**

В данной лабораторной работе, я освоила основные возможности командной оболочки Midnight Commander. Приобрела навыкы практической работы по просмотру каталогов и файлов; манипуляций с ними.



# **Контрольные вопросы (лабораторная работа №8)**

*1. Какие режимы работы есть в mc. Охарактеризуйте их.* 




*2.	Какие операции с файлами можно выполнить как с помощью команд shell, так и с помощью меню (комбинаций клавиш) mc? Приведите несколько примеров.*




*3.	Опишите структура меню левой (или правой) панели mc, дайте характеристику командам.*



*4.	Опишите структура меню ```Файл``` mc, дайте характеристику командам.* 

В меню Файл содержит перечень команд, которые могут быть применены к од- ному или нескольким файлам или каталогам.

Команды меню Файл :

– Просмотр ( F3 ) — позволяет посмотреть содержимое текущего (или выделенного) файла без возможности редактирования.

– Просмотр вывода команды ( М + ! ) — функция запроса команды с параметрами (аргумент к текущему выбранному файлу).

– Правка ( F4 ) — открывает текущий (или выделенный) файл для его редактирования.

– Копирование ( F5 ) — осуществляет копирование одного или нескольких файлов или каталогов в указанное пользователем во всплывающем окне место.

– Права доступа ( Ctrl-x c ) — позволяет указать (изменить) права доступа к од- ному или нескольким файлам или каталогам.

– Жёсткая ссылка ( Ctrl-x l ) — позволяет создать жёсткую ссылку к текущему (или выделенному) файлу.

– Символическая ссылка ( Ctrl-x s ) — позволяет создать символическую ссылку к текущему (или выделенному) файлу.

– Владелец/группа ( Ctrl-x o ) — позволяет задать (изменить) владельца и имя группы для одного или нескольких файлов или каталогов.

– Права (расширенные) — позволяет изменить права доступа и владения для одного или нескольких файлов или каталогов.

– Переименование ( F6 ) — позволяет переименовать (или переместить) один или несколько файлов или каталогов.

– Создание каталога ( F7 ) — позволяет создать каталог.

– Удалить ( F8 ) — позволяет удалить один или несколько файлов или каталогов.

– Выход ( F10 ) — завершает работу mc.

 
*5. Опишите структура меню ```Команда```mc, дайте характеристику командам.* 

В меню Команда содержатся более общие команды для работы с mc.

Команды меню Команда :

– Дерево каталогов — отображает структуру каталогов системы.

– Поиск файла — выполняет поиск файлов по заданным параметрам.

– Переставить панели — меняет местами левую и правую панели.

– Сравнить каталоги ( Ctrl-x d ) — сравнивает содержимое двух каталогов.

– Размеры каталогов — отображает размер и время изменения каталога (по умолчанию в mc размер каталога корректно не отображается).

– История командной строки — выводит на экран список ранее выполненных в оболочке команд.

– Каталоги быстрого доступа ( Ctrl-\ ) — пр вызове выполняется быстрая смена текущего каталога на один из заданного списка.

– Восстановление файлов — позволяет восстановить файлы на файловых системах ext2 и ext3.

– Редактировать файл расширений — позволяет задать с помощью определённого синтаксиса действия при запуске файлов с определённым расширением (например, какое программного обеспечение запускать для открытия или редактирова- ния файлов с расширением doc или docx).

– Редактировать файл меню — позволяет отредактировать контекстное меню пользователя, вызываемое по клавише F2 .

– Редактировать файл расцветки имён — позволяет подобрать оптимальную для пользователя расцветку имён файлов в зависимости от их типа.


*6.	Опишите структура меню ```Настройки``` mc, дайте характеристику командам.* 
 
 Меню Настройки содержит ряд дополнительных опций по внешнему виду и функциональности mc.
 
 
Меню Настройки содержит:

– Конфигурация — позволяет скорректировать настройки работы с панелями.

– Внешний вид и Настройки панелей — определяет элементы (строка меню, командная строка, подсказки и прочее), отображаемые при вызове mc, а также геометрию расположения панелей и цветовыделение.

– Биты символов — задаёт формат обработки информации локальным терминалом.

– Подтверждение — позволяет установить или убрать вывод окна с запросом подтверждения действий при операциях удаления и перезаписи файлов, а также при
выходе из программы.

– Распознание клавиш — диалоговое окно используется для тестирования функциональных клавиш, клавиш управления курсором и прочее.

– Виртуальные ФС –– настройки виртуальной файловой системы:т айм-аут, пароль и прочее.



*7.	Назовите и дайте характеристику встроенным командам mc.* 




*8.	Назовите и дайте характеристику командам встроенного редактора mc.*

Встроенный в mc редактор вызывается с помощью функциональной клавиши F4 . В нём удобно использовать различные комбинации клавиш при редактировании содержимого (как правило текстового) файла.

**Клавиши для редактирования файла**

```Ctrl-y``` удалить строку

```Ctrl-u``` отмена последней операции

```Ins``` вставка/замена

```F7``` поиск (можно использовать регулярные выражения)

```^-F7``` повтор последней операции поиска

```F4``` замена

```F3``` первое нажатие — начало выделения, второе — окончание выделения

```F5``` копировать выделенный фрагмент

```F6``` переместить выделенный фрагмент

```F8``` удалить выделенный фрагмент

```F2``` записать изменения в файл

```F10``` выйти из редактора



*9.	Дайте характеристику средствам mc, которые позволяют создавать меню, определяемые пользователем.*




*10. Дайте характеристику средствам mc, которые позволяют выполнять действия, определяемые пользователем, над текущим файлом.*
