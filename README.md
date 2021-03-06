# *RTUITLAB front project*
![logo](https://user-images.githubusercontent.com/71119074/111702667-ad858480-884d-11eb-8cc9-5558eae2e1dd.jpg)
Последний коммит подчистую стер ридмишник вместе с его коммитом, пишу заново...

Добавление README с некоторым запозданием же не считается за просрочку дедлайна, правда?...

## О проекте
Проект является выполненным вступительным заданием в RTUITLAB по направлению front-end. Узнать подробнее можно по этим ссылкам: 

* [Репозиторий с заданиями](https://github.com/RTUITLab/Recruit)
* [Задание по направлению front-end](https://github.com/RTUITLab/Recruit/blob/master/requirements/front/README.md)

Проект представляет из себя сайт новостного агенства, обладающий серверной частью. Сайт обладает свойствами адаптивности и удобства навигации.

## Использованные технологии
* Angular 11.0.4
* Visual Studio Code
* Figma
* NodeJS 14.15.0
* Angular Bootstrap
* OS Windows 10

## Внешний вид приложения
Помимо отосланного вместе с google формой видео, в котором я вкратце прошелся по все аспектам проекта, я записал отдельное видео, в котором продемонстрировал внешний вид сайта, его функционал и возможности адаптивности. Ссылка на видео:

### [Демонстрация возможностей сайта](https://drive.google.com/file/d/1uBXE4DoPpbu5jqpToZfDTs5_elitD4ye/view?usp=sharing)

Для поверехностной демонстрации приложу скриншоты основных компонентов сайта:

#### Главная страница
![image](https://user-images.githubusercontent.com/71119074/111705303-8761e380-8851-11eb-88c3-8d9e4d699498.png)
![image](https://user-images.githubusercontent.com/71119074/111705482-d14ac980-8851-11eb-8bff-ea17690d33b2.png)

#### Просмотр статьи
![image](https://user-images.githubusercontent.com/71119074/111705534-ec1d3e00-8851-11eb-891e-c654c335ee7f.png)
![image](https://user-images.githubusercontent.com/71119074/111705561-fb03f080-8851-11eb-978a-08ee12f94516.png)

#### Авторизация
![image](https://user-images.githubusercontent.com/71119074/111705613-0e16c080-8852-11eb-8ee9-79d79b87a1d4.png)

#### Изменение статьи
![image](https://user-images.githubusercontent.com/71119074/111705714-2f77ac80-8852-11eb-95e4-b2ae65aae5db.png)

#### Создание статьи
![image](https://user-images.githubusercontent.com/71119074/111705834-5b932d80-8852-11eb-8fc6-d92e79f75aa5.png)

## Функционал приложения
Опять же, подробнее в *[видео](https://drive.google.com/file/d/1uBXE4DoPpbu5jqpToZfDTs5_elitD4ye/view)*, но если вкратце, то сайт обладает такими функциями, как:
* Просмотр всех статей
* Сортировка статей по тегам
* Просмотр конкретной статьи
* Авторизация

Авторизированный пользователь/администратор получает доступ к еще ряду функций:
* Создание статьи
* Редактирование статьи
* Выход из аккаунта

## Техническая реализация
Фреймворк Angular позволяет разбить процесс разработки приложения на более четкие компоненты и этапы, так что разработчик может работать над сервисами и компонентами независимо друг от друга.
Структура проекта выглядит как набор необходимых для работы фреймворка файлов, набор используемых ассетов, и самое главное и особенное в Angular: набор компонентов и сервисов, каждый из которых отвечает за свой собственный функционал в общей структуре приложения. Список созданных в рамках проекта компонентов и сервисов:

* [article.component](https://github.com/666Dallas666/RTULAB_front/tree/main/src/app/components/article)
* [authorization.component](https://github.com/666Dallas666/RTULAB_front/tree/main/src/app/components/authorization)
* [change.component](https://github.com/666Dallas666/RTULAB_front/tree/main/src/app/components/change)
* [create.component](https://github.com/666Dallas666/RTULAB_front/tree/main/src/app/components/create)
* [header.component](https://github.com/666Dallas666/RTULAB_front/tree/main/src/app/components/header)
* [mainpage.component](https://github.com/666Dallas666/RTULAB_front/tree/main/src/app/components/mainpage)
* [shownews.service](https://github.com/666Dallas666/RTULAB_front/tree/main/src/app/services/Shownews)
* [user.service](https://github.com/666Dallas666/RTULAB_front/tree/main/src/app/services/user)

Фото структуры проекта:

![image](https://user-images.githubusercontent.com/71119074/111707481-2c31f000-8855-11eb-926a-c8d53cd6e847.png)

Пройдемся по компонентам и сервисам чуть более подробно:

### header.component
Данный компонент является скелетом сайта и представляет из себя навбар с футером сайта, между которых встроен предоставленный фреймворком Angular router-outlet, позволяющий встраивать остальные компоненты в этот.С точки зрения функционала данный компонент реализует функции поиска статей по тегам, инициирование процесса авторизации, и, само собой, функцию навигации.

### mainpage.component
Как можно понять по названию, данный компонент представляет из себя главную страницу приложения, которая отображает список всех существующих статей. Данный компонент вместе с header.component организует работу с тэгами, отрисовывая лишь нужные статьи, а также принимает статьи с сервера при помощи специального сервиса. Нажав на одну из статей, можно переместиться на следующий компонент.

### article.component
Данный компонент служит для отрисовки конкретной статьи, id которой он получает на вход. Также обращается для этого к серверу при помощи сервиса.

### authorization.component
Без данного компонента не получится повзаимодействовать и идущими ниже компонентами. Компонент представляет из себя форму для авторизации с полями ввода логина и пароля. Не трудно догадаться, что компонент взаимодействует с полями пользователей в базе данных при помощи запросов через специальный сервис. В зависимости от полученного ответа компонент переадресует пользователя на предыдущую страницу, на которой он зашел в ситсему атворизации, либо же выводит оповещение, что введенные данные были неверными.

### change.component
Этот компонент позволяет авторизированному пользователю/администратору контента редактировать выбранную статью (Если пользователь авторизован, на странице article.component появляется клавиша, перенаправляющая пользователя на данную страницу). Компонент представляет из себя форму с заранее заполненными полями ввода, данные для которых получаются при помощи запроса к серверу по конкретной статье. Поля можно редактировать, меняя содержимое заголовка, текста, тэгов и т.д. После изменения интересующх полей нажатие кнопки, подтверждающей изменение статьи, обратится к специальному сервису, который выполнит put-запрос на сервер и передаст ему объекст статьи по нужному id.

### create.component
Данный компонент сильно напоминает своим внешним видом предыдущий. Только он уже позволяет создавать статьи по шаблону, предоставленному формой заполнения, соответстующей представлению статьи в базе данных. После заполнения полей нажатие соответствующей кнопки отправит на сервер post-запрос через специальный сервис.

### shownews.service и user.service
Если вкратце, то при помощи двух данных сервисов все компоненты проекта взаимодействуют с базой данных сервера, получая и посылая данные. Сервисы обрабатывают запросы, связанные с авторизацией и работой со статьями. В них включены функции, делающие либо get-запросы для получения нужных данных, либо post/put запросы, прилагая к их header'ам токен авторизации с припиской 'Bearer'.

### Остальные файлы...
Из оставшихся файлов наиболее часто изменяемыми являются app-routing.module, отвечающий за установку маршрутов между компонентами, и app.module, в который добавляются все компоненты, работающие с методами фреймворка Angular.

## Запуск проекта
Для того, чтобы запустить все это чудо на своей машине, недостаточно будет только скачать архив проекта с GitHub. Для начала вам понадобятся NodeJS и npm. У меня стоит Node версии 14.15.0 и npm версии 6.14.8. После этого при помощи того же npm нужно будет установить сам Angular cli, у меня установлена версия 11.0.4. Далее вам нужно будет установить ряд модулей для проекта. Подробнее об этом можно почитать [здесь](https://angular.io/guide/setup-local). Могут только сказать, что список установленных в проекте модулей можно найти в файле [package-lock.json](https://github.com/666Dallas666/RTULAB_front/blob/main/package-lock.json). Модулей там безумное количество, не уверен, что все они требуются для запуска проекта, в первую очередь рекомендую обратить внимание на данные компоненты:

![image](https://user-images.githubusercontent.com/71119074/111710074-f6433a80-8859-11eb-8458-2eaed86cbc45.png)

После проведенных манипуляций и танцев с бубнами пропишем в терминале проекта следующую команду:

`ng serve`

Далее, если есть желание загрузить на сайте хоть какой-то контент из базы данных, нужно будет запустить сервер, [также находящийся в папке проекта](https://github.com/666Dallas666/RTULAB_front/tree/main/json-server). Для этого переходим в папку с файлом server.json, запускаем там консоль и пишем следующую команду:

`node server.js`

После этого все заработает корректно, и вы сможете насладиться полным функционалом созданного приложения.

## P.S.

### А почему...
Не устану повторять, и повторю еще раз, кто-то украл мой коммит с предыдущей версией README.md, судя по всему мой push последних изменений сделал с ним что-то нехорошее.

### А что за коммиты трехмесячной давности?
А дело все в том, что я создавал данный проект в папке уже существующего, когда я только начинал разбираться с Angular. А сделал я это по той причине, что в том проекте уже была настроена удобная и правильная иерархия папок, а также установлены все нужные модули, что позволило незамедлительно приступить к работе.

### Ну в таком случае почему новых коммитов раз-два и обчелся?
Тут проблема в том, что я не особо внимателен, и долистал до низа документа с набором только тогда, когда разработка приближалась к завершающему этапу. На тот момент я уже не видел смысла загружать что-то промежуточное. Так что основная часть одним коммитом.

## Это кто-то читает?
