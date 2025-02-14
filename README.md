# test1

**Система контроля версий** - это специальное программное обеспечение, которое используется для управления в файловой системе, отслеживания и контроля версий документов или кода программы.

**Преимущества применения системы контроля версий:**
1. История изменений
2. Контроль версий
3. Коллективная работа
4. Ветвление и слияние
5. Отслеживание ошибок


### Распределённая VS Централизованная системы контроля версий ###

**Архитектура:** Централизованная система контроля версий имеет центральную базу данных, где хранятся все файлы и изменения. В распределённой системе каждый пользователь имеет собственную копию репозитория, включая всю историю изменений.

картинка

**Управление правами доступа:** В централизованной системе управление правами доступа к репозиторию обычно происходит на уровне центрального сервера. В распределённой системе каждый пользователь может выполнять операции с собственной копией репозитория, что позволяет более гибко управлять правами доступа.

**Скорость работы:** Распределённая система обычно быстрее выполняет операции, так как все данные хранятся локально у каждого пользователя. В централизованной системе операции происходят через удалённое соединения что может быть медленнее при большом количестве пользователей.

>**Система контроля версий с механизмом снимков** *хранят все версии фалов и директорий в форме полных копий (снимков) состояния проекта в определённый момент времени. Когда вы делаете коммит, система фиксирует все измененные файлы и создает новый снимок, который включает в себя полные копии всех измененных файлов. Это позволяет быстро переключаться между разными версиями проекта и осуществить обход старых коммитов.*

>**Система контроля версий со списком изменений** (например Subversion) хранят только разницу (дельта) между последующими версиями файлов. Когда вы делаете коммит, система сохраняет только изменения, сделанные в файлах, относительно предыдущего коммита, в виде списка изменений. На самом деле, система часто хранит несколько версий файла, чтобы быстрее обрабатывать запросы, основанные на списке изменений. При переключении на предыдущие версии проекта, СКВ применяет все изменения последовательно, чтобы восстановить запрошенную версию проекта.

**Коммит** - операция, при которой изменения сделанные пользователем сохраняются в репозитории проекта. Коммит фиксирует изменения в файле или наборе файлов.
Каждый коммит имеет уникальный идентификатор, который позволяет отслеживать историю изменений и восстанавливать предыдущие версии файлов.

картинка
**Merging** - процесс объединения различных версий файлов.

### Команды для работы с Git ###
```
git init
git status
git log
git config --list
git add $filename$ файл из рабочего -> индексированные файлы
git rm $filename$ удалить из проиндексированные
git commit -m "message"
git diff разница между рабочим каталогом и последним фиксированным состоянием
git diff --staged разница + последний снимок репозитория
```

картинка

картинка

