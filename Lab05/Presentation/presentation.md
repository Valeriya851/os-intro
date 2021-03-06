---
## Front matter
lang: ru-RU
title: Лабораторная работа №5
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

Благодаря данной лабораторной работе появятся практические навыки взаимодействия пользователя с системой посредством командной строки.


# Цель работы

Приобретение практических навыков взаимодействия пользователя с системой посредством командной строки.


# Задания

- Определить полное имя домашнего каталога;
- Перейти в каталог ```/tmp``` и вывести содержимое этого каталога;

```cd /tmp```, ```ls```

- В домашнем каталоге создать новый каталог ```newdir```;

``` cd /home```, ```mkdir newdir```

- В каталоге newdir создать новый каталог ```morefun```;

```cd newdir```, ```mkdir morefun```

# Задания

- В домашнем каталоге создать одной командой три новых каталога и удалить их;

```sudo mkdir letters memos misk```

```sudo rm -r letters memos misk```

- Удалить ранее созданный каталог ```newdir```;

```sudo rm -r newdir```

- С помощью комманды man определить опции ```ls```;

```man ls```


# Задания

- С помощью команды man описать команды: ```cd```, ```pwd```, ```mkdir```, ```rm```;

```man cd```, ```man pwd```, ```man mkdir```, ```man rm```

- Команда ```history```, выполнить модификацию и исполнение нескольких команд из буфера команд

```history```, ```!1385:s/alF/F```, ```cd; ls; pwd```


# Результат

В данной лабораторной работе, я приобрела практические навыки взаимодействия пользователя с системой посредством командной строки.
