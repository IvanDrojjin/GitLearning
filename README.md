# GitLearning
 Git Learn, Traning..

 ##  New string in branch NEW 
 # at local PC
 
git pull "HTTP......"
git branch NEW

git add .\README.md        # at local PC
git commit - m "  my commit"
git push


git pull

https://learn.microsoft.com/ru-ru/azure/devops/boards/github/add-remove-repositories?view=azure-devops
https://docs.github.com/en/repositories/creating-and-managing-repositories/deleting-a-repository
https://learngitbranching.js.org/
https://itproger.com/course/git/5



Урок 3. Работа с удалёнными репозиториями  (https://gb.ru/lessons/305485/homework)
Дополнить файл с инструкцией по работе с git (второе домашнее задание), создать свой открытый репозиторий в github, создать отдельную ветку, туда залить файл с инструкцией и создать pull request из неё в основную ветку.

Файл с инструкцией необходимо дополнить информацией о работе с удаленными репозиториями.
В системе подгрузить скриншот отправленного pull request и ссылку на репозиторий.\


1. Как подключиться к удаленному репозитарию?
Для загрузки данных в удаленный репозитарию сначала нужно к нему подключиться. В нашем примере мы используем адрес https://github.com/tutorialzine/awesome-project, однако пользователь может создать собственный удаленный репозитарий на GitHub, BitBucket или другом подобном сервисе. Это занимает некоторое время, однако в дальнейшем полностью себя оправдывает, тем более, что подобные службы имеют пошаговые инструкции для правильно выполнения нужных действий.
Для того, чтобы связать созданный нами локальный репозитарий с удаленным, выполним такую команду:

# This is only an example. Replace the URI with your own repository address.
$ git remote add origin https://github.com/IvanDrojjin/GitLearning.git 

Первая строка напоминает нам, что URI репозитария, который приведен в примере, нужно изменить на свой.
Иногда бывает так, что проект имеет несколько удаленных репозитариев – в таком случае каждому из них присваивается собственное имя. Главный репозитарий принято называть origin.

2. Как отправить изменения в удаленный репозитарий?
Теперь, когда у нас в локальном репозитарии создан коммит и мы подключились к удаленному, можем отправить его на сервер. Мы это будем делать каждый раз, когда хотим обновить данные в удаленном репозитарии.
Отправка коммита осуществляется с помощью команды push, которая имеет два параметра - имя удаленного репозитория (в нашем случае origin) и ветку, в которую необходимо внести изменения (main — это ветка по умолчанию для всех репозиториев).

$ git push origin main

3. Как клонировать удаленный репозитарий?
Если у других пользователей возникла необходимость клонировать удаленный репозитарий, они могут получить полностью работоспособную копию при помощи команды clone:

$ git clone https://github.com/IvanDrojjin/GitLearning.git

GitHub автоматически создаст новый локальный репозитарий в виде удаленного на собственном сервере.

4. Как запросить изменения с удаленного репозитария?
В случае, если другим пользователям нет необходимости делать клон удаленного репозитария, а нужно просто получить информацию об изменениях, это можно сделать с помощью команды pull:

$ git pull origin master
From https://github.com/IvanDrojjin/GitLearning.git
* branch main -> FETCH_HEAD
  Already up-to-date.

Она скачивает новые изменения.