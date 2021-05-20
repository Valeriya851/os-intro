---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №10"

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







# ***Текстовой редактор emacs***

# **Оглавление:**

1.	Введение:
  a) Цель работы
2.	Описание результатов выполнения задания;
3.	Вывод;
4.	Контрольные вопросы.

























# **Введение:**

Emacs представляет собой мощный экранный редактор текста, написанный на языке высокого уровня Elisp.

*Буфер* — объект, представляющий какой-либо текст.

Буфер может содержать что угодно, например, результаты компиляции програм- мы или встроенные подсказки. Практически всё взаимодействие с пользователем, в том числе интерактивное, происходит посредством буферов.

*Окно* — прямоугольная область фрейма, отображающая один из буферов.

*Область вывода* — одна или несколько строк внизу фрейма, в которой Emacs выводит различные сообщения, а также запрашивает подтверждения и дополнительную информацию от пользователя.

*Минибуфер* используется для ввода дополнительной информации и всегда отображается в области вывода.

*Точка вставки* — место вставки (удаления) данных в буфере ([Источник](https://esystem.rudn.ru/pluginfile.php/1142514/mod_resource/content/3/007-lab_emacs.pdf)).


# **Цель работы:**

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором ```Emacs```.


# **Описание результатов выполнения задания:**


1.  Открыла ```emacs``` *(рис 1.1 и 1.2)*:

```emacs```

   ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/1.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118982619-6b87d480-b99d-11eb-8fdb-ef2906967c12.png))
   
   ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/2.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118982650-7478a600-b99d-11eb-9807-d68f10cd70dd.png))
   
*Рис 1.1 и 1.2. Открытие ```emacs```*

2.	 Создать файл ```lab07.sh``` с помощью комбинации ```Ctrl-x``` ```Ctrl-f``` (```C-x``` ```C-f```) *(рис 2.1)*:
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/создание.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118985744-8c9df480-b9a0-11eb-8958-24dafbe3d877.png))
 
*Рис 2.1. Создание файла*


3.	Набрала текст: *(рис 3.1)*

#!/bin/bash

HELL=Hello function hello {

    LOCAL HELLO=World
    
echo $HELLO }

echo $HELLO

hello
 
![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/4.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118982756-8b1efd00-b99d-11eb-995e-909b775478c3.png))

*Рис 2.1. Набор текста*
 
4.  Сохранила файл с помощью комбинации ```Ctrl-x``` ```Ctrl-s``` (```C-x``` ```C-s```): `


5.	Проделала с текстом стандартные процедуры редактирования: 

 a) Вырезала одной командой целую строку (```С-k```) *(рис 5.1)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/выделение.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118985859-a50e0f00-b9a0-11eb-97d4-87931b7e98b9.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/вырезание.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118985898-ae977700-b9a0-11eb-9bd7-b03afc261e40.png))
 
*Рис 5.1. Вырезание строки*

 b) Вставила эту строку в конец файла (```C-y```) *(рис 5.2)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/вставка.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118985954-bb1bcf80-b9a0-11eb-9f33-2921c4b64765.png))

*Рис 5.2. Вставка строки*

 c) Выделила область текста (```C-space```):


 d) Скопировала область в буфер обмена (```M-w```) *(рис 5.3)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/8.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983039-d46f4c80-b99d-11eb-9f6f-422b4d05cc62.png))

*Рис 5.3. Копирование области в буфер обмена*

 e) Вставила область в конец файла *(рис 5.4)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/9.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983092-e2bd6880-b99d-11eb-8c11-f47e5970586b.png))

*Рис 5.4. Вставка в конец файла*

 f) Вновь выделила эту область и на этот раз вырезала её (```C-w```) *(рис 5.5)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/10.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983147-f072ee00-b99d-11eb-9e8f-98942fcf0cd2.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/9.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983325-1dbf9c00-b99e-11eb-8ebe-b554440aebb4.png))

*Рис 5.5. Выделение и вырезание*

 g) Отмените последнее действие (C-/) *(рис 5.6)*:
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/11.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983361-2adc8b00-b99e-11eb-92bc-f2e96f1166e9.png))

*Рис 5.6. Отмена последнего действия*

6.	Научилась использовать команды по перемещению курсора:

  а) Переместила курсор в начало строки (```C-a```) *(рис 6.1)*:

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/начало.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118986014-cbcc4580-b9a0-11eb-9855-c7b58fdec19d.png))
 
*Рис 6.1. Перемещение курсора*

  b) Переместила курсор в конец строки (```C-e```) *(рис 6.2)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/конец.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118986080-d7b80780-b9a0-11eb-9dca-c5b450f1c67c.png))

*Рис 6.2. Перемещение курсора*

  с) Переместила курсор в начало буфера (M-<) *(рис 6.3)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/13.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983640-75f69e00-b99e-11eb-919c-f7a6dc3c99c2.png))

*Рис 6.3. Перемещение курсора*

  d) Переместила курсор в конец буфера (M->) *(рис 6.4)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/14.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983502-53fd1b80-b99e-11eb-9992-e3bbf72836b6.png))

*Рис 6.4. Перемещение курсора*


7.	Управление буферами: 

   a) Вывела список активных буферов на экран (```C-x``` ```C-b```) *(рис 7.1)*

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/15.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983690-83138d00-b99e-11eb-9fdf-6407de2f6a8c.png))
 
*Рис 7.1. Вывод списка на экран*

   b) Переместила во вновь открытое окно (```C-x```) со списком открытых буферов и переключилась на другой буфер. *(рис 7.2)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/17.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983773-9a527a80-b99e-11eb-9da9-2bf474898730.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/16.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983732-8eff4f00-b99e-11eb-8fe4-c72efc7a49c6.png))

*Рис 7.2. Переключение на другой буфер*

   c) Закрыла это окно (```C-x 0```) *(рис 7.3)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/18.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983857-b229fe80-b99e-11eb-8ada-a0e515e9afe2.png))

*Рис 7.3. Закрыла окно*

   d) Теперь вновь переключилась между буферами, но уже без вывода их списка на экран (```C-x b```) *(рис 7.4)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/19.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983911-c40ba180-b99e-11eb-8e90-1f50909f9798.png))

*Рис 7.4. Переключение между буферами*


8.	Управление окнами:

 a) Поделила фрейм на 4 части: разделила фрейм на два окна по вертикали (C-x 3), а затем каждое из этих окон на две части по горизонтали (C-x 2) *(рис 8.1, 8.2)*

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/20.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118983984-d7b70800-b99e-11eb-8789-6366cb9ca642.png))
 
*Рис 8.1. Разделение на 2 части*

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/21.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118984030-e2719d00-b99e-11eb-9878-5005a0aa42d5.png))
 
*Рис 8.2. Разделение на 4 части*

   b) В каждом из четырёх созданных окон открыла новый буфер (файл) и ввела несколько строк текста *(рис 8.3)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/22.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118984078-f0272280-b99e-11eb-8b1d-f9f3741e1468.png))

*Рис 8.3. Введение текста*

9.  Режим поиска: 

 a) Переключилась в режим поиска (```C-s```) и нашла несколько слов, присутствующих в тексте *(рис 9.1)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/23.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118984118-fb7a4e00-b99e-11eb-86cc-e06f3a4574aa.png))
 
*Рис 9.1. Поиск слов*

 b) Переключилась между результатами поиска, нажимая ```C-s``` *(рис 9.2)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/24.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118984155-0503b600-b99f-11eb-9053-49e94ec3ed72.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/2%20hello.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118985473-4a74b300-b9a0-11eb-9fa2-444f7d630ed7.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/25.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118984211-1220a500-b99f-11eb-9ede-c90f0bbd37ac.png))

*Рис 9.2. Переключение между результатами поиска*

 c) Вышла из режима поиска, нажав ```C-g``` *(рис 9.3)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/27.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118984293-2b295600-b99f-11eb-9f1a-b8af4242d4a6.png))

*Рис 9.3. Выход из режима*

 d) Перешла в режим поиска и замены (```M-%```), ввела текст, который следует найти и заменить, нажала ```Enter``` , затем ввела текст для замены. После того как были подсвечены результаты поиска, нажала ```!``` для подтверждения замены *(рис 9.4, 9.5, 9.6)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/28.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118984344-3bd9cc00-b99f-11eb-971e-ecdce0ee9e46.png))

*Рис 9.4. Переход в режим поиска и замены, и ввод текста, который следует найти*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/29.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118984388-45633400-b99f-11eb-8d3c-0dfc4bf09f93.png))

*Рис 9.5. Ввод текста для замены*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/30.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118984500-5f9d1200-b99f-11eb-939a-464b58a98626.png))

*Рис 9.6. Результат*

 e) Испробовала другой режим поиска, нажав ```M-s o``` *(рис 9.7)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab10/Screenshot/31.png?raw=true![image](https://user-images.githubusercontent.com/83212205/118984548-6a57a700-b99f-11eb-9c00-9186b01630fe.png))

*Рис 9.7. Другой режим поиска*

 Он отличается тем, что внизу экрана выводится окно, где показывает количество предложений в которых нашли это слово. Слово представленное для нахождения подсвечивается желтым. 


# **Вывод:**

В данной лабораторной работе, я познакомилась с операционной системой Linux. Получила практические навыки работы с редактором ```Emacs```.



# **Контрольные вопросы (лабораторная работа №10)**

*1. Кратко охарактеризуйте редактор emacs.* 

Emacs представляет собой мощный экранный редактор текста, написанный на языке высокого уровня Elisp.

*2.	Какие особенности данного редактора могут сделать его сложным для освоения новичком?*

Он не сложен, но обладает огромным количеством разных функций, которые были добавлены за более чем два десятилетия его существования. Само освоение редактора занимает неделю — за это время вы изучите основные приемы редактирования и привыкните к сочетаниям клавиш. Этого будет достаточно, чтобы чувствовать себя комфортно во время работы.

   Второй этап — это выбор среди того множества функций именно тех, что нужны вам для работы. Он может растянуться на месяцы и даже годы. А скорее всего не закончится никогда — для Emacs постоянно выходят новые расширения, которые могут вам пригодиться.



*3.	Своими словами опишите, что такое буфер и окно в терминологии emacs’а.*

*Окно* — прямоугольная область фрейма, отображающая один из буферов.

*Буфер* — объект, представляющий какой-либо текст.


*4.	Можно ли открыть больше 10 буферов в одном окне?* 

У каждого буфера есть имя, которое может быть произвольной длины, и вы можете выбрать любой буфер по имени. Большинство буферов создаются при обращении к файлам, и их имена производятся из имени файла. Но вы можете также создать пустой буфер с любым именем, каким захотите. 

Нет
 
*5. Какие буферы создаются по умолчанию при запуске emacs?* 



*6. Какие клавиши вы нажмёте, чтобы ввести следующую комбинацию C-c | и C-c C-|?* 
 



*7.	Как поделить текущее окно на две части?* 

Разделить фрейм на два окна по вертикали - ```C-x 3```


*8.	В каком файле хранятся настройки редактора emacs?*




*9. Какую функцию выполняет клавиша <- и можно ли её переназначить?*


*10. Какой редактор вам показался удобнее в работе vi или emacs? Поясните почему.*
