# Тестовое задание

Задача заключается в реализации интерфейса audio–плеера.

![player](_img_/player.png)

**Необходимо:**

- Реализовать импортирование библиотеки
- Левое меню
- Нужно собрать интерфейс разделов "Artists" и "Albums".
- Собрать блок управления воспроизведением. 
- Сохранять текущее состояние библиотеки в LocalStorage.
- Переход между разделами не должен приводить к остановке воспроизведения.

Задачи подробнее описаны ниже. Каждая задача состоит из обязательной и дополнительной части (её выполнение не обязательно, однако приносит очень много баллов).

**Требования:**

- При выполнении можно пользоваться Backbone, JQuery, React. Но отдельным плюсом будет использование Vanilla JS, ES2015. Можно использовать любые шаблонизаторы. Использование Typescript будет большим плюсом.
- Код должен работать в последних версиях Chrome, Firefox, Safari, IE10+.
- Нужно может вёрстку, приложенную в папке `templates`. При этом вёрстку можно менять как угодно.
- Результат должен быть выложен на гитхаб и быть доступен через [Github Pages](https://pages.github.com/).

# Задачи

## Импорт библиотеки

![import](_img_/import.png)

* Плеер должен уметь импортировать библиотеку в виде json-файла [library.json](https://raw.githubusercontent.com/VladimirSemenyuk/target-frontend-test/master/library.json).
* Импорт осуществляется с помощью стандартного диалога выбора файла.

***дополнительное задание***

* Показывать какой-нибудь прелоадер, либо прогресс–бар пока json парсится. Приложенный файл библиотеки будет парсится быстро, так что можно добавить задержку с помощью метода setTimeout.

## Левое меню

![left_menu](_img_/left_menu.png)

* Левое меню представляет собой 2 постоянных ссылки на разделы (Artists и Albums), а также блок создания и выбора плейлистов.
* Нужно иметь возможность создавать новые плейлисты, давать им названия. 

***дополнительное задание***

* Добавление песни в плейлист происходит через Drag'n'Drop песни из правого блока плеера в название плейлиста.
* Реализовать поиск по имени исполнителя, по названию песни. Результат поиска - плейлист.

![search](_img_/search.png)

## Отображения трека

![songs](_img_/songs.png)

Стандартное отображение трека должно включать в себя:
* название трека, 
* имя альбома, в который он входит, 
* иконку добавления в плейлист, прии нажатии на которую выпадает спикок плейлистов. Клик на плейлист добавляет песню в него. 

## Раздел "Artists"

![artists](_img_/artists.png)

* В этом разделе должны отображаться песни, сгруппированные по альбомам и по исполнителям. Альбомы должны быть отделены друг от друга заголовком альбома и годом издания, а также его обложкой, а исполнители – именем исполнителя.

***дополнительное задание***

* Добавить возможность прямой и обратной сортировки по имени исполнителя.

## Раздел "Albums"

![albums](_img_/albums.png)

* В этом разделе должны отображаться песни, сгруппированные по альбомам. Альбомы должны быть отделены друг от друга заголовком альбома и годом издания, а также его обложкой.

***дополнительное задание***

* Добавить возможность прямой и обратной сортировки по имени исполнителя, по имени альбома, по году издания.

## Выбранный Playlist

![playlist](_img_/playlist.png)

* В этом разделе должны отображаться песни, добавленные в выбранный плейлист. 

***дополнительное задание***

* Порядок воспроизведения должен настраиваться с помощью Drag'n'Drop.

## Блок управления воспроизведением

![controls](_img_/controls.png)

* Проигрывать музыку не нужно. При взаимодействии с элементами нужно просто логировать в консоль действия пользователя.

***дополнительное задание***

* Сделать имитацию "проигрывания" песни. Примем, что каждая длится 10 секунд. После прохождения этого времени нужно начать "проигрывать" следующую песню в плейлисте или альбоме (в зависимости от того, откуда эта песня была запущена).
