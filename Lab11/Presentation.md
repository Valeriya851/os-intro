---
## Front matter
lang: ru-RU
title: Лабораторная работа №11 (Программирование в командном процессоре ОС UNIX. Командные файлы)
author:
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

Благодаря данной лабораторной работе я изучу основы программирования в оболочке ОС UNIX/Linux. Научусь писать небольшие командные файлы.



# Цель работы

Изучить основы программирования в оболочке ОС UNIX/Linux. Научиться писать небольшие командные файлы.


# Задания

- Написать скрипт, который при запуске будет делать резервную копию самого себя (то есть файла, в котором содержится его исходный код) в другую директорию backup в вашем домашнем каталоге. При этом файл должен архивироваться одним из архиваторов на выбор zip, bzip2 или tar. 

#!/bin/bash

cp lab11.txt backup

echo "Файл с исходным кодом скопирован в директорию backup"

tar --totals -cvf archive.tar lab11.txt

echo "Архивация файла"




# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab11/Screenshot/8.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119552761-b69a5100-bdbc-11eb-8592-a9b4791cdb9b.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab11/Screenshot/10.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119553601-99b24d80-bdbd-11eb-996b-dcb9ed022cbf.png))




# Задания

- Написать пример командного файла, обрабатывающего любое произвольное число аргументов командной строки, в том числе превышающее десять. Напри- мер, скрипт может последовательно распечатывать значения всех переданных аргументов.

#!/bin/bash

echo $1

echo $2

echo $3

echo $4

echo $5

echo $6

echo $7

echo $8

echo $9

echo ${10}

echo ${11}



# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab11/Screenshot/12.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119553014-ffeaa080-bdbc-11eb-8a69-bacc071931e5.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab11/Screenshot/15.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119553923-ebf36e80-bdbd-11eb-99b8-caa96b472953.png))



# Задания

- Написать командный файл — аналог команды ls. Требуется, чтобы он выдавал информацию о нужном каталоге и выводил информацию о возможностях доступа к файлам этого каталога.

#!/bin/bash

for file in *

do

echo -n $file:""

pwd 

done


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab11/Screenshot/17.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119553175-34f6f300-bdbd-11eb-9758-6580b280637f.png))

# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab11/Screenshot/20.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119553726-b8184900-bdbd-11eb-899a-2e24fbfae2e8.png))


# Задания

- Написать командный файл, который получает в качестве аргумента командной строки формат файла (.txt, .doc, .jpg, .pdf и т.д.) и вычисляет количество таких файлов в указанной директории. Путь к директории также передаётся в виде аргумента командной строки.

#!/bin/bash

echo $1

echo $2

find $2 -name "*$1" -print

tree -P "*$1" --prune $2


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab11/Screenshot/22.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119553337-6374ce00-bdbd-11eb-8c6f-7fb0b16e9412.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab11/Screenshot/27.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119554002-03caf280-bdbe-11eb-966e-c025ceb4554f.png))


# Результат

В данной лабораторной работе, я изучила основы программирования в оболочке ОС UNIX/Linux. Научилась писать небольшие командные файлы.
