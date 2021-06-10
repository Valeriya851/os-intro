---
## Front matter
lang: ru-RU
title: Лабораторная работа №15
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

Благодаря данной лабораторной работе я приобрету практические навыкыки работы с именованными каналами.



# Цель работы

Приобретение практических навыков работы с именованными каналами.


# Задания

- Cоздала файлы:

```touch Makefile```

```touch server.c```

```touch client.c```

```touch common.h```


# Задания

Makefile:

  ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab15/Screenshot/4.png?raw=true![image](https://user-images.githubusercontent.com/83212205/121566264-23f5e500-ca3f-11eb-81b5-5633eab6892e.png))
   



# Задания

server.c:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab15/Screenshot/3.png?raw=true![image](https://user-images.githubusercontent.com/83212205/121566227-1b9daa00-ca3f-11eb-958a-d84ec7d59af5.png))

# Задания

client.c:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab15/Screenshot/2.png?raw=true![image](https://user-images.githubusercontent.com/83212205/121566187-12144200-ca3f-11eb-82ed-62382ed028bf.png))


# Задания

common.h:

![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab15/Screenshot/1.png?raw=true![image](https://user-images.githubusercontent.com/83212205/121566139-0759ad00-ca3f-11eb-84a1-c3548c8014db.png))

# Задания

Изучите приведённые в тексте программы server.c и client.c. Взяв данные примеры за образец, напишите аналогичные программы, внеся следующие изменения:

1. Работает не 1 клиент, а несколько (например, два).

2. Клиенты передают текущее время с некоторой периодичностью (например, раз в пять секунд). Используйте функцию sleep() для приостановки работы клиента.

3. Сервер работает не бесконечно, а прекращает работу через некоторое время (например, 30 сек). Используйте функцию clock() для определения времени работы
сервера. Что будет в случае, если сервер завершит работу, не закрыв канал?


# Задания

Измененный Makefile:
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab15/Screenshot/5.png?raw=true![image](https://user-images.githubusercontent.com/83212205/121566309-307a3d80-ca3f-11eb-8b77-52552ffd2e22.png))
 
 # Задания:
 
 Измененный server.c:
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab15/Screenshot/7.png?raw=true![image](https://user-images.githubusercontent.com/83212205/121566389-47209480-ca3f-11eb-8b8a-1bfcfc7aaaee.png))
 

# Задания

Измененный client.c:
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab15/Screenshot/6.png?raw=true![image](https://user-images.githubusercontent.com/83212205/121566354-3bcd6900-ca3f-11eb-99af-3749c41dc719.png))
 
 
 # Задания
 
 Измененный common.h:
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/Lab15/Screenshot/9.png?raw=true![image](https://user-images.githubusercontent.com/83212205/121566481-615a7280-ca3f-11eb-8a20-4c22e2d16c46.png))
 

# Результат

В данной лабораторной работе, я приобрела практические навыки работы с именованными каналами.

