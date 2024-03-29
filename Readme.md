# Инструкция по работе с Git

## Что такое Git

Git -это одна из реализаций распределленых систем контроля версий,что позволяет иметь версионность как локально,так и в удаленном репозитории.Git является самой популярной системой контроля версий.

## Подготовка репозитория

Для создания репозитория использую команду "git init".Втерменале в папке с будующим репозиторием достаточно написать "git init",и эта папка станет репозиторием.

## Состояние репозитория 

Для того чтобы посмотреть состояние репозитория используется команда "git status".Для этого в терминале спапкой-репозиторием нужно написать "git status",и возмодно увидеть несколько состояний:
 1.Nothing to commit - репозиторий не содержит изменений.
 2.Unversioned file - папкамсодержит файл,к которому не добавленна версионность

## Создание комитов

git commit - это команда для записи индексированных изменений в репозиторий Git.

Создать коммит (commit) - значит зафиксировать изменения любых файлов, входящих в репозиторий.

Любые файлы, созданные или измененные вами и для которых вы не выполнили git add после редактирования, не войдут в ваш коммит. Они останутся измененными файлами на вашем диске.


### Добавление файла в коммит
Для добавления файла в коммит используется команда "git add".Для этого достаточно в терменале с папкой текущего репозитория написать *git add <название файла>*.

### Сохранение коммита
Для сохраненния коммита используется команда "git commit" -m "<Сообщение к коммиту>".Сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***

## Журнал изменений

Для просмотра историй коммитов,то есть истории наших изменений используется команда "git log".Для этого необходимо в терменале с папкой-репозиторием написать "git log".

## Перемещение между сохранениями

Для того чтобы перемещатся между комитами необходимо использовать команду "git checkout".Для этого в терминале с папкой репозитория необходимо написать "git checkout<номер коммита>.Номер коммита берется из истории.После такого"пермещения" мы попадаем в состояние **detached head**.Для возвращения в обычное состояние используется команда *git checkout master*.


## Ветки в Git

В Git ветки — это элемент повседневного процесса разработки. По сути ветки в Git представляют собой указатель на снимок изменений. Если нужно добавить новую возможность или исправить ошибку (незначительную или серьезную), вы создаете новую ветку, в которой будут размещаться эти изменения. Объединить нестабильный код с основной базой кода становится сложнее, к тому же перед слиянием с основной веткой можно очистить историю работы над возможностью.

## Слияние веток и решение конфликтов

Слияние веток – это перенос изменений с одной ветки на другую. При этом слияние не затрагивает сливаемую ветку, то есть она остается в том же состоянии, что позволяет нам потом продолжить работу с ней.

Для того чтобы выполнить слияние веток в терменале нужно перейти на ветку мастер выполнив команду "git checkout master" убедится что мы находимся на верной ветке набрав команду "git branch",и только после этого выполнить слияние веток набрав комманду "git merge <имя сливаемой ветки>

*Системы контроля версий предназначены для управления дополнениями, вносимыми в проект множеством распределенных разработчиков. Иногда один и тот же контент могут редактировать сразу несколько разработчиков. Если разработчик A попытается изменить код, который редактирует разработчик B, может произойти конфликт.Git позволяет выполнять слияния очень просто. В большинстве случаев Git самостоятельно решает, как автоматически интегрировать новые изменения.Но бывают случаи когда Git не может автоматически определить,какое изменение является правильныи.Git помечает файл как конфликтующий и останавливает процесс слияния. В этом случае ответственность за разрешение конфликта несут разработчики.
Git предлагает несколько вариантов решения конфликта:

1. Оставить первый вариант
2. Выбрать фторой вариант
3. Или ставить оба варианта

---------------------------------------------------

 Так мы можем в ручную решить конфликтную ситуацию

 --------------------------------------------------

## Удаление веток

После того как  завершаем работу в ветке и соливаем ее с основной базой кода, эту ветку можно будет удалить без потери истории:
Для этого в терменале репозитория нужно ввести комманду "git branch -d branch <название ветки>

## Получение удаленного репозитория 

-----------------------------------------

Длятого чтобы скачать удаленный репозиторий необходимо использовато команду "git clone".В терменале,в котором открыта любая пустая папка,необходимо написать git clone <ссылка на репозиторий>.Репозиторий скачивается в папку,название которой будет совпадать с названием репозитоя 

## Отправка изменений в удаленный репозиторий

ДЛя отправки изменений вудалёный репозиторий,необходимо использовать команду *git push*.Для этого втерменале спапкой срепозиторием пишем команду *git push origin <название ветки>*,<название ветки> - это ветка в удаленном репозитории,куда необходимо отправить совершённые изменения.

## Скачивание изменений с удаленного репозитория

----------------------------------------

Для того чтобы скачать изменения с удаленного репозитория,необходимо использовать команду *git pull*.Втерменале в папке срепозиторием,связанным с удалённым репозиторием,пишем команду *git pull origin <название ветки>*,для того чтобы принять изенения из указанной ветки удаленного репозитория в текущую ветку.

------------------------------------------