# Работа с Github

Перед началом работы делаем резервную копию проекта. 
Если вы уже начали работать с гитом, но что-то не получается, лучше начать с начала.

Инструкция проверена от начала и до конца и если в точности следовать тому, что здесь написано, у вас все получится.

## 1. Создание репозитория

Создаем новый репозиторий на github

![Alt text](https://monosnap.com/file/xbGe5PxImnrxsr4sUvrrWcOD1VlPXw.png)

Указываем имя репозитория, ставим галочку **Initialize this repository with a README**

![Alt text](https://monosnap.com/file/FzJX4QoHicFrojlKtjfMSizPrmSU8i.png)

Изменяем readme.md файл используя MARKDOWN разметку: указываем в нем
* Свое ФИО
* Имя наставника
* Название курса

![Alt text](https://monosnap.com/file/SIIyCxOH6eEx2sYDmZXSa63Rb83jEP.png)
![Alt text](https://monosnap.com/file/tzsWdCI1ngyy5bhbXjkCgFuk5bmwnn.png)
![Alt text](https://monosnap.com/file/7I7LeBbaKJ2jT9C8rvjAaHXRgmXULb.png)

## 2. Работа с репозиторием на компьютере

Копируем адресс репозитория 

![Alt text](https://monosnap.com/file/T6Ge6WJagW6lrSQAO4ghCeqxx5ZsHC.png)

Открываем терминал и заходим в папку с проектом

Пишем (вместо адресса моего репозитория ставите то что скопировали):
```{r, engine='bash', count_lines}
git clone https://github.com/xaosaki/loft-burgers.git .
```
![Alt text](https://monosnap.com/file/vclZGXwj4PkOn0xHRrR20QSpovzz0Z.png)


Работаем над проектом (вставляем файлы, делаем какие-то изменения)

После делаем 

```{r, engine='bash', count_lines}
git add .
git commit -m "Текст коммита"
```

![Alt text](https://monosnap.com/file/ltBiHHnlIEfxFAL0FtEdd51NvWLhhq.png)

Коммит создан (изменения зафиксированы локально)

Делаем push изменений в удаленный репозиторий 

```{r, engine='bash', count_lines}
git push --set-upstream origin master
```

![Alt text](https://monosnap.com/file/9AMMK3qcLaLDM8qHeIvlNEQeQDhi9n.png)

## 3. Проверка работы

Заходим в настройки репозитория 
1. Переходим на вкладку settings
2. Выбираем ветку master. Нажимаем save
3. Копируем получившуюся ссылку

![Alt text](https://monosnap.com/file/W1KiTARqXUoyXfAq5TrRbeE2UpQSIF.png)

Возвращаемся во вкладку обзора репозитория, дописываем ссылку в README
*(Файл редактируется так же, как и в первый раз см. пару пунктов выше)*
![Alt text](https://monosnap.com/file/Q1boNimbnxCTwhDhQC05vg3RCjDNJk.png)

**Проверяем по ссылке, что pages работают**

**Пишем наставнику, что сделали ДЗ и даем ссылку на github, ждем ответа.**

## 4. Работа дальше

Если вы изменили репозиторий на гит-хабе(поменяли readme или работали с другого компьютера)
на основном компьютере перед началом работы нужно сделать 
```{r, engine='bash', count_lines}
git pull
```

Далее работаем, коммитим изменения и пушим их в удаленный репозиторий.

