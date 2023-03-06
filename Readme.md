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

## Слияние веток 
Для слияния веток используется команда *git merge*. Для этого в терминале с папкой-репозиторием необходимо написать *git merge <имя ветки>*. Сливаются текущая открытая ветка с той веткой, название которой прописано в команде. Текущую ветку можно отследить в интерфейсе программы слева снизу, либо командой *git branch* - выведется весь список веток (нужная нам ветка будет выделена другим цветом).

## Разрешение конфликтов
Обычно конфликты возникают, когда несколько человек работают в разных ветках и изменяют одни и те же строки в файле, тогда среда разработки не знает какое изменение является правильным и выдает conflict state - процесс слияния останавливается. Конфликты затрагивают только того разработчика, который выполняет слияние, остальная часть команды о конфликте не знает. 

В нашем файле появляются новые дополнения:

```
<<<<<< HEAD

\=======

\>>>>>>> <имя ветки>"
```

Эти новые строки можно рассматривать как «разделители конфликта». Строка **=======** является «центром» конфликта. Все содержимое между этим центром и строкой **<<<<<<< HEAD** находится в текущей ветке, на которую ссылается указатель *HEAD*. А все содержимое между центром и строкой **>>>>>>> <имя ветки>** является содержимым ветки для слияния.

Самый простой способ разрешить конфликт — отредактировать конфликтующий файл. Просто удалим все разделители конфликта. После редактирования файла выполним команду *git add <имя файла>*. Для завершения слияния создадим новый коммит, выполнив следующую команду: *git commit -m "имя коммита"*.

Git обнаружит, что конфликт разрешен, и создаст новый коммит слияния для завершения процедуры слияния.

## Удаление веток
Для удаления ветки используется команда *git branch -d*. Для того чтобы удалить ветку необходимо в терминале с открытой папкой-репозиторием написать *git branch -d <имя ветки>*.
