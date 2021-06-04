---
## Front matter
lang: ru-RU
title: Лабораторная работа №14
author: |
	Тулеева Валерия, НБИбд-01-20
institute: |
	\inst{1}RUDN University, Moscow, Russian Federation
	
## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---



# Прагматика

Благодаря данной лабораторной работе я приобрету простейшие навыки разработки, анализа, тестирования и отладки приложений в ОС типа UNIX/Linux на примере создания на языке программирования С калькулятора с простейшими функциями.


# Цель работы

Приобрести простейшие навыки разработки, анализа, тестирования и отладки приложений в ОС типа UNIX/Linux на примере создания на языке программирования С калькулятора с простейшими функциями.

# Задания

- В домашнем каталоге создать подкаталог ~/work/lab_prog;

```mkdir lab_prog```

- Создать в нём файлы: calculate.h, calculate.c, main.c:

```touch calculate.h```

```touch calculate.c```

```touch main.c```
 

- Реализовать функции калькулятора в файле calculate.c:


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/Снимок%20экрана%202021-06-04%20в%2020.49.39.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120820752-a2054800-c576-11eb-906c-7e971d65f0bd.png))



# Задания

- Интерфейсный файл calculate.h, описывающий формат вызова функции- калькулятора:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/Снимок%20экрана%202021-06-04%20в%2020.50.00.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120820831-b47f8180-c576-11eb-8adc-6aca9169cbd0.png))


# Задания

- Основной файл main.c, реализующий интерфейс пользователя к калькулятору:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/Снимок%20экрана%202021-06-04%20в%2020.49.51.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120820788-ab8eb000-c576-11eb-8264-ad23abe0e7cd.png))
 
 
 
# Задания

- Выполнить компиляцию программ ыпосредством ```gcc```:

     ```gcc -c calculate.c```
     
      ```gcc -c main.c```
      
     ``` gcc calculate.o main.o -o calcul -lm```
     
- При необходимости исправить синтаксические ошибки.

# Задания

- Создать Makefile со следующим содержанием:

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab14/Screenshot/5.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120824421-42a93700-c57a-11eb-8cca-a7fccfed64c4.png))
 
 # Задания

- С помощью ```gdb``` выполнить отладку программы ```calcul```:

– Запустить отладчик GDB, загрузив в него программу для отладки:

```gdb ./calcul```

– Для запуска программы внутри отладчика ввести команду run:

```run```

– Для постраничного (по 9 строк) просмотра исходного код использовать команду list:

```list```

 # Задания
 
- Установить точку останова в файле calculate.c на строке номер 21:

```list calculate.c:20,27```

```break 21```

– Вывести информацию об имеющихся в проекте точка останова:

 ```info breakpoints```
 
- Убрать точки останова:
  
```info breakpoints```

```delete 1```

 # Задания

- С помощью утилиты ```splint``` попробывать проанализировать коды файлов ```calculate.c``` и ```main.c```.

 
# Результат

В данной лабораторной работе, я приобрела простейшие навыки разработки, анализа, тестирования и отладки приложений в ОС типа UNIX/Linux на примере создания на языке программирования С калькулятора с простейшими функциями.
