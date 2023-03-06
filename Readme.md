# Инструкция по работе с Git

## Что такое Git?
Git - наиболее популярная реализация распределенной системы контроля версий. Алгоритм работы подобных систем схож.

## Подготовка репозитория
Для создания репозитория в папке предполагаемого репозитория необходимо написать команду *git init*. Для этого в терминале с открытой папкой-репозиторием пишем *git init*.

## Создание коммитов

### Добавление файлов к коммиту
Для добавления файлов к коммиту используется команда *git add*. Для того чтобы добавить файл к новому коммиту необходимо в терминале с открытой папкой-репозиторием написать *git add <имя файла>*.

### Создание коммитов
Для создания коммитов используется команда *git commit*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git commit -m "<сообщение к коммиту>"*. Сообшение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

## Журнал изменений
Для просмотра истории изменений используется команда *git log*. Для этого в терминале необходимо с папкой-репозиторием набрать *git log*.

## Перемещение между коммитами
Для перемещения между коммитами используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <номер коммита>*. Номера коммитов можно посмотреть в истории коммитов, описанной в предыдущем пункте.

## Ветки в Git

### Просмотр списка веток
Для просмотра списка веток используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать команду *git branch*.

### Переход между ветками
Для перехода между ветками используется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходимо написать *git checkout <название ветки>*.

### Создание новой ветки
Для создания новой ветки используется команда *git branch*. Для этого в терминале с папкой-репозиторием необходимо написать *git branch <название ветки>*.

## Слияние веток и разрешение конфликтов

## Удаление веток

Удаление веток можно призводить путем прописывания команды 'git branch -d <название ветки, которую нужно удалить>' 
