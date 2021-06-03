---
## Front matter
lang: ru-RU
title: Лабораторная работа №13 
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


# ***Программирование в командном процессоре ОС UNIX. Расширенное программирование***
# Прагматика

Благодаря данной лабораторной работе я изучу основы программирования в оболочке ОС UNIX. Научусь писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.


# Цель работы

Изучить основы программирования в оболочке ОС UNIX. Научиться писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.


# Задания

- Реализовать команду man с помощью командного файла. Изучите содержимое каталога /usr/share/man/man1. В нем находятся архивы текстовых файлов, содержащих справку по большинству установленных в системе программ и команд. Каждый архив можно открыть командой less сразу же просмотрев содержимое справки. Командный файл должен получать в виде аргумента командной строки название команды и в виде результата выдавать справку об этой команде или сообщение об отсутствии справки, если соответствующего файла нет в каталоге man1.


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/7.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631288-8708da00-c489-11eb-9291-d666d7d366b5.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/10.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631391-a56ed580-c489-11eb-99ee-38318d01c544.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/11.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631426-af90d400-c489-11eb-877a-45e3266e1ddb.png))

# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/13.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631527-cdf6cf80-c489-11eb-8bfb-9524bdfc2fe1.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/14.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631564-d7803780-c489-11eb-8f1f-5891eca66eb9.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/15.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631628-e8c94400-c489-11eb-946b-48bb7e5d8903.png))

# Задания

- Используя встроенную переменную $RANDOM, напишите командный файл, генерирующий случайную последовательность букв латинского алфавита.

# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/26.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120632158-7c027980-c48a-11eb-865e-1c330be80bba.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/27.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120632287-9c323880-c48a-11eb-92d5-e6b156966f5f.png))




# Задания

- Написать командный файл. Командный файл должен в течение некоторого времени t1 дожидаться освобождения ресурса, выдавая об этом сообщение, а дождавшись его освобождения, использовать его в течение некоторого времени t2. Запустить командный файл в одном виртуальном терминале в фоновом режиме, перенаправив его вывод в другой (> /dev/tty#, где # — номер терминала куда перенаправляется вывод), в котором также запущен этот файл, но не фоновом, а в привилегированном режиме. 

# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/1.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631004-32655f00-c489-11eb-839a-45f4cba210bc.png))

# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/2.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631062-4315d500-c489-11eb-8201-858e0ef7d4f2.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/6.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631224-76586400-c489-11eb-8a01-5eb3aa092bca.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/3.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631124-532db480-c489-11eb-9802-8edf586df411.png))


# Задания

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab13/Screenshot/4.png?raw=true![image](https://user-images.githubusercontent.com/83212205/120631154-5c1e8600-c489-11eb-8bdd-c0038459854b.png))




# Результат

В данной лабораторной работе, я изучила основы программирования в оболочке ОС UNIX. Научилась писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.
