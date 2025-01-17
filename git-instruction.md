# Инструкция по работе с git
![Официальный логотип git](logo.png)

## Lesson 1

## Что такое git и контроль версий
**Системы контроль версий** - это системы, которые: 
1. обеспечивают сохранение содержимого файлов и папок(их *версий*)
2. Обеспечивают передвижение по *версиям* этих файлов и папок

**git** - это самая известная и используемая на данный момент реализация контроля версий с командным интерфейсом

**Локальный репозиторий** - это хранилище *изменений* Git в виде папки.

## Инициализация локального репозитория

Для того чтобы сказать git, что данная папка является локальным репозиторием нужно зайти в папку и ввести в ней команду

*git init*

Также, если этого раньше не делалось, то нужно определить ваше имя пользователя и email командами:
. git config --global user.name "your name"
. git config --global user.email your email 

## Добавление файлов под контроль версий

Для этого нужно ввести команду:
*git add имена файлов*
Теперь имена и содержимое этих файлов можно сохронять

## Делаем коммит

Для того, чтобы изменения представляли собой отдельную версию, к которой можно возвращаться и манипулировать после добавления под **контроль версий**, нужно ввести команду:

*git commit -m "Название версии"*

Можно также добавить под контроль версий и сформировать коммит для всех  файлов и папок одной командой:
*git commit -am "Название версии"

## Просмотр текущего состояния репозитория
Для вывода текущего состояния локального репозитория используются команды:

>git status - просмотр состояния файлов и папок в репозитории

> git diff - просмотр самих изменений файлов и папок

## Просмотр всех изменений репозитория

Для просмотра истории изменений от начала и последнего коммита нужно ввести:

*git log*

git status - команда, вывод состояния репозитория
git init - иницыализация git
## Lesson 2
## работа с ветками в git
git branch - выводит ветки
branch
git branch name - создание ветки
Github

Данила

## Альтернативные системы контроля версий:

[DVC, или Data Version Control](https://habr.com/ru/companies/skillfactory/articles/527510/), — это один из многих доступных инструментов с открытым исходным кодом, упрощающих работу с проектами Data Science и ML.

Используется подход Git'а в том смысле, что дает интерфейс командной строки, который настраивается в несколько простых шагов. DVC, как предполагает его название, фокусируется не только на версионировании данных. Инструмент помогает командам управлять конвейерами и моделями машинного обучения. В конце концов, DVC способствует согласованности вашей команды и воспроизводимости ваших моделей.

**Преимущества**

1. **Лёгкий**, исходники открыты, подходит для всех основных облачных платформ и типов хранилищ данных.
2. **Гибкий**, независимый от формата и фреймворка, лёгкий в применении.

**Недостатки**

1. Контроль версий DVC тесно связан с управлением конвейером. Это означает, что, если ваша команда уже применяет другой инструмент конвейера данных, будет **дублирование**.
2. DVC **лёгкий**, это означает, что вашей команде, возможно, придётся **вручную разработать дополнительные функции**.



### Delta Lake

[Delta Lake](https://delta.io/) — это слой хранилища с открытым исходным кодом, помогающий улучшить состояние озёр данных. Это делается предоставлением транзакций ACID, версионированием данных, управлением метаданными и управлением версиями данных. Инструмент находится ближе к слою абстракции озёр данных, заполняя пробелы там, где большинство озёр данных ограничены.

Преимущества

1. Предлагает множество функций, которые могут не входить в вашу систему хранения данных, например ACID-транзакции или эффективное управление метаданными.

2. Снижает необходимость в ручном управлении версиями данных и ручном решении других связанных с данными вопросов, позволяя разработчикам сосредоточиться на построении продуктов поверх озёр данных.

Недостатки

1. Delta Lake часто бывает перегибом для большинства проектов: инструмент был разработан для работы со Spark на больших данных.

2. Требуется специальный формат данных, а это означает, что инструмент теряет в гибкости и зависим в отношении текущих форматов.
Основная задача инструмента — действовать в качестве скорее уровня абстракции данных, а это может быть не тем, что нужно вашей команде, и также может игнорировать разработчиков, которым нужно решение легче.

[Другие альтернативы](https://habr.com/ru/companies/skillfactory/articles/527510/) 

# Версия инструкции Быкасова Алена
## Инструкция по работе с Git
## Lesson 1
## *Добавляем команды*

1. Gti add - добавить версионность
2. - Git commit -m "Название изменеий"
    - Git commit -am "Название изменений" (одна команда для Add и comit)
3. Git log - проверить все созданные комиты
4. Q - выход из команды git log
5. * Git checkout 567y - вернуться к определенному коммиту
    * Git checkout master - вернуться к окончательной версии (со всеми ветками) 
6. Git init - инициализация гати
7. Git status - команда, вызывающая блок информации по состоянию реппозитоия
8. git diff — показать разницу между версиями
Показывает разницу между текущим файлом
и сохранённым

  ##  Lesson 2 
Git Branch - выводит ветки 

Создать ветку можно командой git branch.

Делать это надо в папке с репозиторием: 
branch - ветка
Git branch name - создание ветки

Если потребуется переключиться с одной ветки
на другую, вызовем команду git checkout <имя
ветки>

 Конфликт изменений
 
При работе в двух ветках одновременно может
возникнуть ситуация, когда в одной и другой
ветке мы по-разному изменили блок текста.
Если затем мы попробуем слить эти ветки, Git
сообщит о конфликте и предложит выбрать,
какие же изменения записать.
## Lesson 3
1. *git clone* - команда загружает все изменения, но и пытается слить
все ветки на локальном компьютере и в
удаленном репозитории
2. *git pull* - команда позволяет скачать все из текущего репозитория и автоматически
сделать merge с нашей версией
3. *git push* - команда отправляет свою версию репозитория во внешний репозиторий поможет команда.
 * При первом её использовании нужна авторизация.
 4. *pull request*
* команда для предложения изменений
* запрос на вливание изменений в репозиторий
Как сделать pull request
* Делаем   (ответвление) репозитория fork
* Делаем git clone   версии репозитория СВОЕЙ
* Создаем новую ветку и в НЕЕ вносим свои изменения
* Фиксируем изменения (делаем коммиты)
* Отправляем свою версию в свой GitHub
* На сайте GitHub нажимаем кнопку pull reques