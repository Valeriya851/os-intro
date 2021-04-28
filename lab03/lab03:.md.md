
РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ
Факультет физико-математических и естественных наук
Кафедра прикладной информатики и теории вероятностей





ОТЧЕТ ПО ЛАБОРАТОРНОЙ РАБОТЕ № 2

Дисциплина:	Операционные системы	 







                                               Преподаватель: Кулябов Дмитрий Сергеевич

                                               Студент: Тулеева Валерия                                    

                                               Группа: НБИбд-01-20                                       







МОСКВА
2021 г.


***Управление версиями***

**Оглавление:**

1.	Введение:
  a) Основные команды git
  b) Цель работы
2.	Описание результатов выполнения задания;
3.	Вывод;
4.	Библиография.

























**Введение:**

Системы контроля версиями записывают и сохраняют несколько изменений в файлах. Благодаря этому можно вернуться к определенной точке истории изменения файла или проекта. Некоторые системы, такие как Subversion, отслеживают историю отдельных файлов. Другие, такие как Git и Mercurial, отслеживают историю целых репозиториев.
Управление версиями подобно системе безопасности. Если вы внесли изменения, которые позже вызвали проблемы, можно будет вернуть файл или весь проект к определенной точке вместо того, чтобы начинать все с нуля.
Распределенное управление версиями является популярным благодаря таким системам, как Git и Mercurial. Они широко применяются для организации совместной работы в проектах с открытым исходным кодом. Из-за особенностей настройки клонирование всей базы кода проекта для каждой равноправной системы позволяет получить больше свободы, когда дело касается рабочих процессов и совместной работы.
Система контроля Git представляет собой набор программ командной строки. 

**Основные команды git:**

***Наиболее часто используемые команды git:***

- создание основного дерева репозитория:
```git init```

- получение обновлений(изменений)текущего дерева из центрального репозитория: 
```git pull```

- отправка всех произведённых изменений локального дерева в центральный репозиторий:
```git push```

- просмотр списка изменённых файлов в текущей директории: 
```git status```

- просмотр текущих изменения: 
```git diff```

- mдобавить все изменённые и/или созданные файлы и/или каталоги:
```git add .```

-добавить конкретные изменённые и/или созданные файлы и/или каталоги: 
```git add имена_файлов```

- удалить файл и/или каталог из индекса репозитория (при этом файл и/или каталог остаётся в локальной директории):
```git rm имена_файлов```

- сохранить все добавленные изменения и все изменённые файлы:
```git commit -am 'Описание коммита'```

- сохранить добавленные изменения с внесением комментария через встроенный
редактор:
```git commit```

- создание новой ветки,базирующейся нат екущей: 
```git checkout -b имя_ветки```

- переключение на некоторую ветку: 
```git checkout имя_ветки```

(при переключении на ветку, которой ещё нет в локальном репозитории, она будет
создана и связана с удалённой)

- отправка изменений конкретной ветки в центральный репозиторий:
```git push origin имя_ветки```

- слияние ветки с текущим деревом:
```git merge --no-ff имя_ветки```

- удаление локальной уже слитой с основным деревом ветки:
```git branch -d имя_ветки```

- принудительное удаление локальной ветки: 
```git branch -D имя_ветки```


**Цель работы:**

Изучить идеологию и применение средств контроля версий. 


**Описание результатов выполнения задания:**

1.	Установила команду git:

```sudo apt install git``` *(рис 1.1)*
 
 ![Рис 1.1. Установка](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/1:.png)

*Рис 1.1.Установка*

2.	Вручную устранила проблемы:

```sudo dpkg --configure -a ```*(рис 2.1)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/2:.png)
 
*Рис 2.1. Устранение проблемы*

3.	Создала учетную запись на [github](https://github.com): *(рис 3.1 и рис 3.2)*

![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/4:.png)
 
*Рис 3.1. Создание учетной записи*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/5:.png)
 
*Рис 3.2*

4.	Создала локальный репозиторий: *(рис 4.1)*

```git config --global user.name “Tuleeva Valeriya”```

```git config --global user.email leratuleeva@gmail.com```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/3:.png)
 
*Рис 4.1. Создание локального репозитория*

5.	Создала репозиторий на Github и назвала его os-intro: *(рис 5.1)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/6:.png)
 
*Рис 5.1. Создание репозитория на сайте*

6.	Создала каталог work и в нем каталог laboratory: *(рис 6.1)*

```mkdir work```

```cd work```

```mkdir laboratory```

```cd laboratory```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/7:.png)
 
*Рис 6.1. Каталоги*

7.	Инициализировала систему git: *(рис 7.1)*

```git init```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/8:.png)
 
*Рис 7.1. Инициализация*

8.	Создала заготовку для файла README.md: *(рис 8.1)*

```echo “# Лабораторные работы” >> README.md```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/9:.png)
 
*Рис 8.1. Создание заготовки для файла*

9.	Сделала первый коммит и выложила на github: *(рис 9.1 и рис 9.2)*

```git commit -m “first commit”```

```git remote add origin git@github.com:Valeriya851/sciproc-intro.git```

```git push -u origin master```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/12:.png)
 
*Рис 9.1. Создание первого коммита*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/36:.png.png)
 
*Рис 9.2*

10.	 Добавила файл лицензии: *(рис 10.1)*

```wget https://creativecommons.org/licenses/by/4.0/legalcode.txt -O LICENSE```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/13:.png?raw=true![image](https://user-images.githubusercontent.com/83212205/116371962-c8c0b800-a82d-11eb-853d-5a5c0f6612e8.png)
)
 
*Рис 10.1. Добавление файла лицензии*

11.	Добавила шаблон игнорируемых файлов: *(рис 11.1)*

```curl -L -s https://www.gitignore.io/api/list```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/17:.png)
 
*Рис 11.1. Шаблон игнорируемых файлов*

12.	 Скачала шаблон С: *(рис 12.1 и рис 12.2)*

```curl -L -s https://www.gitignore.io/api/c >> .gitignore```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/16:.png)
 
*Рис 12.1. Скачивание шаблона С*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/37:.png.png?raw=true![image](https://user-images.githubusercontent.com/83212205/116392696-8e154a80-a842-11eb-8283-4b5ce27cd0c6.png))

 
*Рис 12.2. Генерация файла*

13.	Добавила новые файлы: *(рис 13.1)*

```git add .gitignore```
      
      Выполнила коммит:
```git commit -m```
      
      Отправила на github:
```git push```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/11:.png)
 
*Рис 13.1*

14.	 Сгенерировала ключ: *(рис 14.1)*

```ssh-keygen -t ed25519 -C leratuleeva@gmail.com```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/18:.png)
 
*Рис 14.1. Генерация ключа*

15.	 Установила xclip: *(рис 15.1)*

```sudo apt install xclip```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/19:.png)
 
*Рис 15.1. Установка*

16.	 Скопировала ключ: *(рис 16.1)*

```cat ~/.ssh/id_ed25519.pub | xclip -selclip```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/20:.png)
 
*Рис 16.1. Копирование ключа*

17.	 Вставила ключ в появившееся на сайте поле. *(рис 17.1)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/21:.png)
 
*Рис 17.1*

18.	 Загрузила git-flow: *(рис 18.1)*

```sudo apt-get install git-flow```

 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/25:.png)
 
*Рис 18.1. Установка*

19.	 Инициализировала git-flow: *(рис 19.1)*

```git flow init```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/26:.png)
 
*Рис 19.1. Инициализация*

20.	 Проверила, что я на ветке develop: *(рис 20.1)*

```git branch```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/27:.png)
 
*Рис 20.1*

21.	 Создала релиз с версией 1.0.0: *(рис 21.1)*

```git flow release start 1.0.0```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/28:.png)
 
*Рис 21.1. Создание релиза*

22.	 Записала версию: *(рис 22.1)*

```echo “1.0.0” >> VERSION```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/29:.png)
 
*Рис 22.1. Запись*

23.	 Добавила в индекс: *(рис 23.1)*

```git add .```

```git commit -am ‘chore(main): add version’```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/31:.png)
 
*Рис 23.1. Добавление*

24.	 Залила релизную ветку в основную ветку: *(рис 24.1)*

```git flow release finish 1.0.0```
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/32:.png)
 
*Рис 24.1*

25.	 Отправила данные на github:

```git push –all``` *(рис 25.1)*

```git push –tags``` *(рис 25.2)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/33:.png)
 
*Рис 25.1*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/34:.png)
 
*Рис 25.2*

26.	 Репозиторий *(рис 26.1)*
 
 ![](https://github.com/Valeriya851/os-intro/blob/os-intro/lab03/screenshots/35:.png)
 
*Рис 26.1*


**Вывод:**

В данной лабораторной работе, я изучила идеологию и применение средств контроля версий. 

**Библиография:**

https://www.internet-technologies.ru/articles/newbie/chto-takoe-upravlenie-versiyami.html

https://esystem.rudn.ru/user/policy.php
