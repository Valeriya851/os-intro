---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №14"

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







# ***Средства, применяемые при разработке программного обеспечения в ОС типа UNIX/Linux***

# **Оглавление:**

1.	Введение:
  a) Цель работы
2.	Описание результатов выполнения задания;
3.	Библиография;
4.	Вывод;
5.	Контрольные вопросы.

























# **Введение:**

*Этапы разработки приложений*

Процесс разработки программного обеспечения обычно разделяется на следующие этапы:

– планирование, включающее сбор и анализ требований к функционалу и другим характеристикам разрабатываемого приложения;

– проектирование,включающеевсебяразработкубазовыхалгоритмовиспецификаций, определение языка программирования;

– непосредственная разработка приложения:

– кодирование — по сути создание исходного текста программы (возможно в нескольких вариантах);

– анализ разработанного кода;

– сборка, компиляция и разработка исполняемого модуля;

– тестирование и отладка, сохранение произведённых изменений;

– документирование.

Для создания исходного текста программы разработчик может воспользоваться
любым удобным для него редактором текста: vi, vim, mceditor, emacs, geany и др. После завершения написания исходного кода программы (возможно состоящей из нескольких файлов), необходимо её скомпилировать и получить исполняемый модуль. 
[Источник](https://esystem.rudn.ru/pluginfile.php/1142526/mod_resource/content/2/011-lab_prog.pdf)

Стандартным средством для компиляции программ в ОС типа UNIX является GCC (GNU Compiler Collection).

Это набор компиляторов для разного рода языков программирования (С, C++, Java, Фортран и др.). Работа с GCC производится при помощи одноимённой управляющей программы gcc, которая интерпретирует аргументы командной строки, определяет и осуществляет запуск нужного компилятора для входного файла.
Файлы с расширением (суффиксом) .c воспринимаются gcc как программы на языке С, файлы с расширением .cc или .C — как файлы на языке C++, а файлы c расширением .o считаются объектными.

[Источник](https://esystem.rudn.ru/pluginfile.php/1142526/mod_resource/content/2/011-lab_prog.pdf)


# **Цель работы:**

Приобрести простейшие навыки разработки, анализа, тестирования и отладки приложений в ОС типа UNIX/Linux на примере создания на языке программирования С калькулятора с простейшими функциями.

# **Описание результатов выполнения задания:**


1.  В домашнем каталоге создайте подкаталог ~/work/lab_prog*(рис 1.1 и 1.2)*:

```cd ~/work```

```mkdir lab_prog```

   ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/1.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824227-0c6bb780-c57a-11eb-92cd-9d828f592838.png))
   
*Рис 1.1. Создание подкаталога*

2.	Создала в нём файлы: calculate.h, calculate.c, main.c *(рис 2.1 и 2.2)*:

```cd lab_prog```

```touch calculate.h```

```touch calculate.c```

```touch main.c```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/2.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824280-1beb0080-c57a-11eb-8ffa-9275f378da63.png))
 
*Рис 2.1. Создание файлов*


3.	 Реализовала функций калькулятора в файле calculate.c*(рис 3.1)*

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/Снимок%20экрана%202021-06-04%20в%2020.49.39.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120820752-a2054800-c576-11eb-906c-7e971d65f0bd.png))
 
 *Рис 3.1. Реализация*
 
4.  Интерфейсный файл calculate.h, описывающий формат вызова функции- калькулятора *(рис 4.1)*: `

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/Снимок%20экрана%202021-06-04%20в%2020.50.00.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120820831-b47f8180-c576-11eb-8adc-6aca9169cbd0.png))

*Рис 4.1. Интерфейсный файл*


5.	Основной файл main.c, реализующий интерфейс пользователя к калькулятору: *(рис 5.1)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/Снимок%20экрана%202021-06-04%20в%2020.49.51.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120820788-ab8eb000-c576-11eb-8264-ad23abe0e7cd.png))
 
*Рис 5.1. Основной файл*


6.	Выполнила компиляцию программы посредством ```gcc```*(рис 6.1)*:

```gcc -c calculate.c```

```gcc -c main.c```
      
```gcc calculate.o main.o -o calcul -lm```

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/3.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824332-2c02e000-c57a-11eb-807e-c83bbcf63917.png))
 
*Рис 6.1. Компиляция*


7.	Создала Makefile: *(рис 7.1)*

```touch Makefile```

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/4.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824370-34f3b180-c57a-11eb-8832-025c952222ce.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/5.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824421-42a93700-c57a-11eb-8cca-a7fccfed64c4.png))
 
*Рис 7.1. Makefile*

**Код:**


```#Makefile```

  ```CC = gcc```                             *(Переменные)*
  
  ```CFLAGS =```
  
  ```LIBS = -lm```
  
```calcul: calculate.o main.o```                *(calcul - цель, calculate.o & main.o - названия файлов, которые мы хотим скомпилировать)*

```gcc calculate.o main.o -o calcul $(LIBS)``` *(команда компиляции gcc с опциями)*

```calculate.o: calculate.c calculate.h```      *(calculate.o - цель, calculate.c & calculate.h - названия файлов, которые мы хотим скомпилировать)*

```gcc -c calculate.c $(CFLAGS)```              *(команда компиляции gcc с опциями)*

```main.o: main.c calculate.h```                 *(main.o - цель, main.c & calculate.h - названия файлов, которые мы хотим скомпилировать)*

```gcc -c main.c $(CFLAGS)```                     *(команда компиляции gcc с опциями)*

```clean:```                           *(Цель с именем clean производит очистку каталога от файлов, полученных в результате компиляции)*

   ```-rm calcul *.o *~```
          
  ```#End Makefile```


8.	С помощью ```gdb``` выполните отладку программы ```calcul```:

- Запустила отладчик GDB, загрузив в него программу для отладки *(рис 8.1)*:

```gdb ./calcul```

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/6.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824460-4d63cc00-c57a-11eb-973d-d05dd1baa1f2.png))
 
 *Рис 8.1. Запуск отладчика*
 
- Для запуска программы внутри отладчика ввела команду ```run``` *(рис 8.2)*:

```run```

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/7.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824502-594f8e00-c57a-11eb-9c11-38047981bf41.png))

*Рис 8.2. Запуск программы*

- Для постраничного (по 9 строк) просмотра исходного код использовала команду list *(рис 8.3)*:

```list```

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/9.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824613-71271200-c57a-11eb-89bb-6ab4b9880468.png))

*Рис 8.3. Просмотр кода*

- Установила точку останова на строке номер 21 *(рис 8.4)*:

```break 21```

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/10.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824671-7c7a3d80-c57a-11eb-9ea0-3ebabe489c37.png))

*Рис 8.4. Точка останова*

- Выведите информацию об имеющихся в проекте точка останова *(рис 8.5)*:
       
```info breakpoints```

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/11.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824709-856b0f00-c57a-11eb-8eca-8259d17d9611.png))

*Рис 8.5. Вывод информации*

- Посмотрела, чему равно на этом этапе значение переменной ```Numeral```, введя:

```print Numeral```
  
На экране было выведено число 5.

- Убрала точки останова *(рис 8.6)*:

```info breakpoints```

```delete 1```

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/12.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824750-8ef47700-c57a-11eb-8f69-4468d465a988.png))

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/13.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824803-9b78cf80-c57a-11eb-9f76-25eaa9411b87.png))

*Рис 8.6. Удаление точки отсанова*


9.  С помощью утилиты ```splint``` попробуйте проанализировать коды файлов ```calculate.c``` и ```main.c``` *(рис 9.1 и 9.2)*: 

```sudo apt install splint``` (установка утилиты ```splint```) *(рис 9.0)*:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/14.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824881-ab90af00-c57a-11eb-9188-69e577cc9a86.png))

*Рис 9.0. Установка*

```splint calculate.c```*(рис 9.1)*:
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/16.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824998-c6632380-c57a-11eb-8e90-223db12d02dc.png))
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/17.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120825033-cebb5e80-c57a-11eb-94ec-af68fdd38051.png))

*Рис 9.1. Код ```calculate.c```*

```splint main.c```*(рис 9.2)*:
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/15.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824930-b5b2ad80-c57a-11eb-8d30-ae568ba0346e.png))

*Рис 9.2. Код ```main.c```*


# **Библиография:**

1. [Источник 1](https://esystem.rudn.ru/pluginfile.php/1142526/mod_resource/content/2/011-lab_prog.pdf)


# **Вывод:**

В данной лабораторной работе, я приобрела простейшие навыки разработки, анализа, тестирования и отладки приложений в ОС типа UNIX/Linux на примере создания на языке программирования С калькулятора с простейшими функциями.



# **Контрольные вопросы (лабораторная работа №14)**

*1. Как получить информацию о возможностях программ gcc, make, gdb и др.?* 

Дополнительную информацию о этих программах можно получить с помощью функций info и man.

*2.	Назовите и дайте краткую характеристику основным этапам разработки приложений в UNIX.*

*Этапы разработки приложений*

Процесс разработки программного обеспечения обычно разделяется на следующие этапы:

– планирование, включающее сбор и анализ требований к функционалу и другим характеристикам разрабатываемого приложения;

– проектирование,включающеевсебяразработкубазовыхалгоритмовиспецификаций, определение языка программирования;

– непосредственная разработка приложения:

– кодирование — по сути создание исходного текста программы (возможно в нескольких вариантах);

– анализ разработанного кода;

– сборка, компиляция и разработка исполняемого модуля;

– тестирование и отладка, сохранение произведённых изменений;

– документирование.


*3.	Что такое суффикс в контексте языка программирования? Приведите примеры использования.*

Файлы с расширением (суффиксом) .c воспринимаются gcc как программы на языке С, файлы с расширением .cc или .C — как файлы на языке C++, а файлы c расширением .o считаются объектными.

Таким образом, gcc по расширению (суффиксу) .c распознает тип файла для компиляции и формирует объектный модуль — файл с расширением .o.



*4.	Каково основное назначение компилятора языка С в UNIX?* 

Стандартным средством для компиляции программ в ОС типа UNIX является GCC (GNU Compiler Collection). Это набор компиляторов для разного рода языков программирования (С, C++, Java, Фортран и др.). Работа с GCC производится при помощи одноимённой управляющей программы gcc, которая интерпретирует аргументы командной строки, определяет и осуществляет запуск нужного компилятора для входного файла.

 
*5. Для чего предназначена утилита make?* 

Для сборки разрабатываемого приложения и собственно компиляции полезно воспользоваться утилитой make. Она позволяет автоматизировать процесс преобразования файлов программы из одной формы в другую, отслеживает взаимосвязи между файлами.
Для работы с утилитой make необходимо в корне рабочего каталога с Вашим проектом создать файл с названием makefile или Makefile, в котором будут описаны правила обработки файлов Вашего программного комплекса.

*6. Приведите пример структуры Makefile. Дайте характеристику основным элементам этого файла.* 
 
В самом простом случае Makefile имеет следующий синтаксис: 

<цель_1> <цель_2> ... : <зависимость_1> <зависимость_2> ...

           <команда 1>
          
          ...
          
          <команда n>
          
Сначала задаётся список целей, разделённых пробелами, за которым идёт двоеточие и список зависимостей. Затем в следующих строках указываются команды. Строки с командами обязательно должны начинаться с табуляции.
В качестве цели в Makefile может выступать имя файла или название какого-то действия. Зависимость задаёт исходные параметры (условия) для достижения указанной цели. Зависимость также может быть названием какого-то действия. Команды — собственно действия, которые необходимо выполнить для достижения цели.


*7.	Назовите основное свойство, присущее всем программам отладки. Что необходимо сделать, чтобы его можно было использовать?* 

Для использования GDB необходимо скомпилировать анализируемый код про- граммы таким образом, чтобы отладочная информация содержалась в результирующем бинарном файле. Для этого следует воспользоваться опцией -g компилятора gcc:

gcc -c file.c -g

После этого для начала работы с gdb необходимо в командной строке ввести одноимённую команду, указав в качестве аргумента анализируемый бинарный файл:
gdb file.o

*8.	Назовите и дайте основную характеристику основным командам отладчика gdb.*


![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/Снимок%20экрана%202021-06-04%20в%2022.00.35.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120830530-67a0a880-c580-11eb-8ab1-2ad301158900.png))



*9. Опишите по шагам схему отладки программы, которую Вы использовали при выполнении лабораторной работы.*

- Выполнила компиляцию программы посредством gcc:

      gcc -c calculate.c
      
      gcc -c main.c
      
      gcc calculate.o main.o -o calcul -lm
      
- При необходимости исправила синтаксические ошибки.
 
- Создала Makefile со следующим содержанием:


#Makefile 

  CC = gcc
  
  CFLAGS =
  
  LIBS = -lm
  
calcul: calculate.o main.o

gcc calculate.o main.o -o calcul $(LIBS)

calculate.o: calculate.c calculate.h gcc -c calculate.c $(CFLAGS)

main.o: main.c calculate.h

gcc -c main.c $(CFLAGS)

clean:

          -rm calcul *.o *~
          
  #End Makefile
  
*10. Прокомментируйте реакцию компилятора на синтаксические ошибки в программе при его первом запуске.*

Выводит информацию об ошибках.

*11. Назовите основные средства, повышающие понимание исходного кода программы.*

*12. Каковы основные задачи, решаемые программой splint?*
