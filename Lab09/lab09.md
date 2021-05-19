---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №9"

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







# ***Текстовой редактор vi***

# **Оглавление:**

1.	Введение:
  a) Цель работы
2.	Описание результатов выполнения задания;
3.	Вывод;
4.	Контрольные вопросы.

























# **Введение:**

В большинстве дистрибутивов Linux в качестве текстового редактора по умол- чанию устанавливается интерактивный экранный редактор ```vi``` (Visual display editor).

Редактор ```vi``` имеет три режима работы:

– *командный режим* — предназначен для ввода команд редактирования и навигации по редактируемому файлу;

– *режим вставки* — предназначен для ввода содержания редактируемого файла; 

– *режим последней (или командной) строки* — используется для записи изменений в файл и выхода из редактора.

Для вызова редактора ```vi``` необходимо указать команду vi и имя редактируемого файла:

```vi <имя_файла>``` [(Источник)](https://esystem.rudn.ru/pluginfile.php/1142511/mod_resource/content/2/006-lab_vi.pdf)


# **Цель работы:**

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.

# **Описание результатов выполнения задания:**

# **Задание 1. Создание нового файла с использованием vi**

1.  Создала каталог с именем ```lab06```*(рис 1.1 и 1.2)*:

```mkdir lab06```

   ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/1.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118825374-70d11a80-b8dc-11eb-8dcf-61c906dfb8a8.png))
   
*Рис 1.1. Создала каталог ```lab06```*


2.	 Перешла в этот каталог ```lab06```:

```cd lab06```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/cd%20lab06.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118823095-86454500-b8da-11eb-8795-0fa87df2390b.png))
 
*Рис 2.1. Перешла в каталог ```lab06```*


3.	Вызвала ```vi``` и создала файл ```hello.sh```: *(рис 3.1)*


![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/2.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118825428-7d557300-b8dc-11eb-9ca1-25e9c924c8a9.png))
 
*Рис 3.1. Вызов ```vi``` и создание файла ```hello.sh```*

 
4.  Нажала клавишу ```i``` и ввела текст *(рис 4.1)*: `

#!/bin/bash

HELL=Hello

function hello {

    LOCAL HELLO=World
    
echo $HELLO }

echo $HELLO

hello

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/4.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118825513-8fcfac80-b8dc-11eb-85eb-08f7922a81a0.png))

*Рис 4.1. Ввод текста (```i```)*

 
5.	Нажала клавишу ```Esc``` для перехода в командный режим после завершения ввода текста: *(рис 5.1)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/5.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118825582-9c540500-b8dc-11eb-9c0d-f29ce7fa7be1.png))
 
*Рис 5.1. Переход в командный режим (```Esc```)*


6.	Нажала ```:``` для перехода в режим последней строки и внизу моего экрана появилось приглашение в виде двоеточия *(рис 6.1)*:

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/6.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118825627-a7a73080-b8dc-11eb-8100-697a1998371f.png))
 
*Рис 6.1. Переход в режим последней строки (```:```)*


7.	Нажала ```w``` (записать) и ```q``` (выйти), а затем нажала клавишу ```Enter``` для сохранения моего текста и завершения работы.: *(рис 7.1)*

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/7.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118825679-b55cb600-b8dc-11eb-9493-20265f624358.png))

*Рис 7.1. Запись (```w```) и выход (```q```)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/8.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118825731-c0174b00-b8dc-11eb-9a5b-b85c249e57a1.png))

*Рис 7.2. Завершение работы*


8.	Сделала файл исполняемым:

```chmod +x hello.sh```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/9.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118825783-cc030d00-b8dc-11eb-9357-eaa458ac12f0.png))

*Рис 8.1. Исполняемый файл*



# Задание 2. Редактирование существующего файла

1.  Вызвала ```vi``` на редактирование файла *(рис 1.1)*: 

```vi hello.sh```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/10.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118825828-d7563880-b8dc-11eb-8b9b-361375762143.png))

*Рис 1.1. Вызов на редактирование*


2.	Установила курсор в конец слова ```HELL``` второй строки *(рис 2.1)*:

```2``` + (```Shift``` + ```G```)

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/11.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118825884-e2a96400-b8dc-11eb-8e65-8da4c9e23b1b.png))

*Рис 2.1. Установка курсора*


3.	Перешла в режим вставки и заменила на ```HELLO```. Нажала ```Esc``` для возврата в командный режим *(рис 3.1)*:

```i```;

```Esc```;

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/12.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118826009-f5bc3400-b8dc-11eb-943c-06539b03b8e4.png))

*Рис 3.1. Замена слова*


4.  Установите курсор на четвертую строку и стерла слово LOCAL:

```4``` + (```Shift``` + ```G```) *(рис 4.1)*;

```Shift``` + ```x``` *(рис 4.2)*;

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/13.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118826125-07054080-b8dd-11eb-8573-bd669a6dcaf4.png))

*Рис 4.1. Установка курсора на четвертую строку*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/14.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118826181-12586c00-b8dd-11eb-9fab-81dc17ca3bfe.png))

*Рис 4.2. Стирание*

5.  Перешла в режим вставки и набрала следующий текст: ```local```, нажала ```Esc``` для возврата в командный режим *(рис 5.1)*:

```i```;

```Esc```;

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/15.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118826253-243a0f00-b8dd-11eb-93fa-d09249cd3c06.png))

*Рис 5.1. Набор текста ```local```*

6.  Установила курсор на последней строке файла. Вставила после неё строку, содержащую следующий текст: ```echo hello``` :

```Shift``` + ```G``` *(рис 6.1)*;

```i``` *(рис 6.2)*;

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/16.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118826359-3ddb5680-b8dd-11eb-8b99-572cf280614a.png))

*Рис 6.1. Установка курсора на последнюю строку*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/17.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118826390-46339180-b8dd-11eb-8e99-2398d65990f6.png))

*Рис 6.2. Вставка текста*

7.  Нажала ```Esc``` для перехода в командный режим *(рис 7.1)*:

```Esc```;

8.  Удалила последнюю строку *(рис 8.1)*:

(```Shift``` + ```d```) + ```0```;

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/18.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118826512-5e0b1580-b8dd-11eb-9d7c-7691188bb1ee.png))

*Рис 8.1. Удаление последней строки*

9.  Ввела команду отмены изменений ```u``` для отмены последней команды *(рис 9.1)*:

```Shift``` + ```u```;

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/19.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118826584-6e22f500-b8dd-11eb-805d-b09cbe0d84d2.png))

*Рис 9.1. Отмена последней команды*

10. Ввела символ ```:``` для перехода в режим последней строки. Записала произведённые изменения и вышла из ```vi```

```:```;

```w``` + ```q```;

```Enter```;

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/21.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118826650-7b3fe400-b8dd-11eb-8b2e-530563efed93.png))

*Рис 10.1. Запись и выход*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab09/Screenshot/22.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118826697-86930f80-b8dd-11eb-99e8-d60d417b71a9.png))

*Рис 10.2. Завершение*




# **Вывод:**

В данной лабораторной работе, я познакомилась с операционной системой Linux. Получила практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.




# **Контрольные вопросы (лабораторная работа №9)**

*1. Дайте краткую характеристику режимам работы редактора vi.* 


*2.	Как выйти из редактора, не сохраняя произведённые изменения?*



*3.	Назовите и дайте краткую характеристику командам позиционирования.*



*4.	Что для редактора vi является словом?* 


 
*5. Каким образом из любого места редактируемог офайла перейти в начало (конец) файла?* 



*6. Назовите и дайте краткую характеристику основным группам команд редактирования.* 
 



*7.	Необходимо заполнить строку символами $. Каковы ваши действия?* 



*8.	Как отменить некорректное действие, связанное с процессом редактирования?*




*9. Назовите и дайте характеристику основным группам команд режима последней строки.*



*10. Как определить, не перемещая курсора, позицию, в которой заканчивается строка?*



*11. Выполните анализ опций редактора vi (сколько их, как узнать их назначение и т.д.).*


*12. Как определить режим работы редактора vi?*


*13. Постройте граф взаимосвязи режимов работы редактора vi.*
