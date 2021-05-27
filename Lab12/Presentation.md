---
## Front matter
lang: ru-RU
title: Лабораторная работа №12
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

Благодаря данной лабораторной работе я изучу основы программирования в оболочке ОС UNIX. Научусь писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.




# Цель работы

Изучить основы программирования в оболочке ОС UNIX. Научится писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.


# Задания

- Используя команды getopts grep, написать командный файл, который анализирует командную строку с ключами:

– -iinputfile — прочитать данные из указанного файла;

– -ooutputfile — вывести данные в указанный файл;

– -pшаблон — указать шаблон для поиска;

– -C — различать большие и малые буквы;

– -n — выдавать номера строк.


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/2.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119791064-4abc0380-bef6-11eb-8b07-7f996bba2126.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/4.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119791168-61625a80-bef6-11eb-91c6-2828ca99333f.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/5.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119791202-6c1cef80-bef6-11eb-8824-3a4b4a2fe7ce.png))


# Задания

- Написать на языке С++ программу, которая вводит число и определяет, является ли оно больше нуля, меньше нуля или равно нулю. Затем программа завершается с помощью функции exit(n), передавая информацию в о коде завершения в оболочку. Командный файл должен вызывать эту программу и, проанализировав с помощью команды $?, выдать сообщение о том, какое число было введено.



# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/7.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119791352-9373bc80-bef6-11eb-91c6-c336b3c34080.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/8.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119791407-9f5f7e80-bef6-11eb-83fd-638679de01b6.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/9.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119791489-b1412180-bef6-11eb-93c4-e791b4ae3b62.png))



# Задания

- Написать командный файл, создающий указанное число файлов, пронумерованных последовательно от 1 до N (например 1.tmp, 2.tmp, 3.tmp,4.tmp и т.д.). Число файлов, которые необходимо создать, передаётся в аргументы командной строки. Этот же командный файл должен уметь удалять все созданные им файлы (если они существуют).

# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/10.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119791606-c8800f00-bef6-11eb-980b-d2fc70aeefcb.png))

# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/11.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119791668-d766c180-bef6-11eb-97b2-72cf44c09c30.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/12.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119791790-f6fdea00-bef6-11eb-85b0-701c3dda673c.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/13.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119791834-00875200-bef7-11eb-8461-f2e7dd4a8137.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/14.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119791872-08df8d00-bef7-11eb-8d3f-d909c3fe9071.png))


# Задания

- Написать командный файл, который с помощью команды tar запаковывает в архив все файлы в указанной директории. Модифицировать его так, чтобы запаковывались только те файлы, которые были изменены менее недели тому назад (использовать команду find).


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/15.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119791956-1dbc2080-bef7-11eb-8b4b-36cb6f1baf8c.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/16.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119792011-2876b580-bef7-11eb-9063-a6fdb3ec8d0d.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab12/Screenshot/17.png?raw=true![image](https://user-images.githubusercontent.com/83212205/119792041-31678700-bef7-11eb-94bb-b05d8ae54a9d.png))


# Результат

В данной лабораторной работе, я изучила основы программирования в оболочке ОС UNIX. Научилась писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.


