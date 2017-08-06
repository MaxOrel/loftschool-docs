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

![Alt text](https://monosnap.com/file/jBnLcyekkxoWt04QnjDjzF8pspuhW5.png)

Открываем терминал и заходим в папку с проектом

Пишем (вместо адресса моего репозитория ставите то что скопировали):
```{r, engine='bash', count_lines}
git clone https://github.com/xaosaki/burgers.git .
```
![Alt text](https://monosnap.com/file/EaBSVDLZ2gwAHe49gACKssULuFaFcy.png)

Локально создаем новую ветку 

```{r, engine='bash', count_lines}
git checkout -b week_1
```
![Alt text](https://monosnap.com/file/ZY1fDBTGBEuOfbm27awSlcCYKhueHk.png)

Работаем в этой ветке (вставляем файлы из сохраненной папки если они раньше были)

После делаем 

```{r, engine='bash', count_lines}
git add .
git commit -m "Текст коммита"
```

![Alt text](https://monosnap.com/file/82wNEn02c6jnq5EWPXBIY7kex4AOKi.png)

Коммит создан

Делаем push изменений в удаленный репозиторий 

```{r, engine='bash', count_lines}
git push --set-upstream origin week_1
```

![Alt text](https://monosnap.com/file/gaqX6fvC1H3SAsbQRVVQR1qzeU8L0y.png)

## 3. Проверка работы

Создаем новую ветку gh-pages
![Alt text](https://monosnap.com/file/x1bY6VEVKxouDjPKhzcKjtaJETt0pg.png)

Заходим с настройки репозитория 
1. Переходим на вкладку settings
2. Выбираем ветку gh-pages. Нажимаем save
3. Копируем получившуюся ссылку

![Alt text](https://monosnap.com/file/drNxFjiNVN2k2tzDxYBQBcGoAUlf7l.png)

Возвращаемся во вкладку обзора репозитория, **обращаем внимание что бы находились в ветке week_1**, дописываем ссылку в README
*(Файл редактируется так же, как и в первый раз см. пару пунктов выше)*
![Alt text](https://monosnap.com/file/QPcKwPJBBbNaTDlGKbBvjdo5G65tJi.png)

Создаем pull request из week_1 в master
![Alt text](https://monosnap.com/file/HBTgrI4SwCVgldc0jpnbz2uClzUNbR.png)
![Alt text](https://monosnap.com/file/Y9l9Bfg0vz2XbpeJ4FkWZtwt5xK6lG.png)

**Публикуем изменения на github pages**

В консоли пишем 

```{r, engine='bash', count_lines}
git push origin week_3:gh-pages
```
*week_3 заменяем на текущую недельную ветку*

![Alt text](https://monosnap.com/file/I1TlQjAAhpSax2hVuuak0s8D6Rg79r.png)

На гите появится вот такая запись 

![Alt text](https://monosnap.com/file/d5AkrLfa6xJynyHUMc05kKJRiKaoXN.png)

**Добавляем настаника в collaborators**
1. Открываем вкладку Settings
2. Переходим в раздел collaborators
3. Пишем ник настаника 
4. Жмем на кнопку

![Alt text](https://monosnap.com/file/OWYFxcS64yWED1JecFXbtnkgoAFo2j.png)

**Пишем наставнику, что все сделали, ждем ответа.**

## 4. Доработка

В окне pull request наставник напишет замечания
После необходимо снова зайти в терминал и написать (так мы стянем изменения readme файла) 
```{r, engine='bash', count_lines}
git pull
```

Далее делаем доработки, коммитим их и пушим.(не забываем сделать пуш в gh-pages ветку) 

Новый pull request создавать не нужно, изменения подтянутся в прошлый. 

**Пишем наставнику, что все поправили, ждем ответа.**

## 5. Новые задания

После того как настаник примет задание вашей первой недели и смержит в мастер все изменения. Вы переключаетесь на мастер и делаете pull
```{r, engine='bash', count_lines}
git checkout master
git pull
```

Далее создаете ветку week_2 
```{r, engine='bash', count_lines}
git checkout -b week_2
```
Работаете в ней, делаете коммит и пуш на удаленный репозиторий 

Создаете новый pull request и снова пишите настанику

