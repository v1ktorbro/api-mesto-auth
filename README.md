# Бэк для проекта [Mesto-auth](https://github.com/v1ktorbro/mesto-auth)
**[ Base URL: mesto-auth.abrosimov.site/api ]**

## Инструменты :

**NODE.JS, EXPRESS.JS, MONGODB, NGINX, UBUNTU, POSTMAN.**
## Руты:

### Публичные:

* Авторизоваться

      POST /signin/{BODY}
      _____________________
      {BODY} = email, password

* Зарегистрироваться

      POST /signup/{BODY}
      _____________________
      {BODY} = email, password

### Приватные:
*P.S. Доступны только после авторизации и получении JWT*

#### /cards
* Получить все карточки

      GET /cards

* Создать карточку

      POST /cards/{BODY}
      _____________________
      {BODY} = name, link

* Удалить карточку

      DELETE /cards/:id

* Поставить лайк карточке

      PUT /cards/:id/likes

* Удалить лайк у карточки

      DELETE /cards/:id/likes

#### /users

* Получить список всех пользователей

      GET /users

* Получить данные конкретного пользователя с :id

      GET /users/:id

* Изменить информацию о аунтифицированном пользователе

      PATCH /users/me/{BODY}
      ______________________
      {BODY} = name, about

* Изменить аватар аунтифицированного пользователя

      PATCH /users/avatar/{BODY}
      ______________________
      {BODY} = link

### Структура проекта:
    controllers/     | обработчики карточек и юзеров;
    errors/          | конструкторы ошибок со статусами;
    middlewares/     | логгеры запросов и аунтефикация пользователя;
    models/          | схема модели карточки и юзера;
    routes/          | маршруты;
    logs/            | логи ошибок и запросов;
    .env             | генерация токена и его хранение в переменной окружения.

*[Репозиторий фронта](https://github.com/v1ktorbro/mesto-auth)*
