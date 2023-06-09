# **Yatube blog API**
API для блога Yatube
***
## Описание проекта:
Проект *API Yatube* - это *API* для проектра *Yatube*, только без фронтенда и view-функции приложения posts.

С помощью *API Yatube* можно запрашивать данные о постах, группах, комментариях в социальной сети *Yatube*, а также создавать новые.

*Yatube*- это учебный проект курса "Python-разработчик" от Яндекс-Практикума, который представляет собой социальную сеть с возможностью публикации постов и подписки на авторов.
***
## **Описание API**
**API для сайта Yatube. Позволяет работать со следующими сущностями:**
- **Посты:**
  + Получить список всех публикаций;
  + Создать новую публикацию;
  + Получить публикацию по id;
  + Обновить публикацию по id;
  + Частично обновить публикацию по id;
  + Удалить публикацию по id.
- **Комментарии к постам:**
  + Получить список всех комментариев публикации;
  + Создать новый комментарий для публикации;
  + Получить комментарий для публикации по id;
  + Обновить комментарий для публикации по id;
  + Частично обновить комментарий для публикации по id;
  + Удалить комментарий для публикации по id.
- **JWT-токен:**
  + Получить JWT-токен;
  + Обновить JWT-токен.
- **Подписка:**
  + Получить список всех подписчиков;
  + Создать подписку;
- **Группы:**
  + Получить список всех групп;
  + Создать новую группу.
***

## **Доступные методы:**

### POSTS

`/api/v1/posts/ (GET, POST)`

`/api/v1/posts/{post_id}/ (GET, PUT, PATCH, DELETE)`

### Comments

`/api/v1/posts{post_id}/comments/ (GET, POST)`

`/api/v1/posts{post_id}/comments/{comment_id}/ (GET, PUT, PATCH, DELETE)`

### Auth

`/api/v1/auth/token/ (POST)`

`/api/v1/auth/token/refresh/ (POST)`

### Follow 

`/api/v1/follow/ (GET, POST)`


### Group

`/api/v1/group/ (GET, POST)`


Автор: Гараев Фархад
## Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
```
'git clone git@github.com:PARTYNEXTDOORS/api_final_yatube.git'
```
```
'cd api_final_yatube'
```

Cоздать и активировать виртуальное окружение:

```
'python -m venv venv'
```
```
'source venv/Scripts/activate'
```

Установить зависимости из файла requirements.txt:

```
'python -m pip install --upgrade pip'
```
```
'pip install -r requirements.txt'
```

Выполнить миграции:

```
'python3 manage.py migrate'
```

Запустить проект на локальном сервере:

```
'python manage.py runserver'
```
## Примеры запросов к API:
Получить список всех постов (GET):

```
http://127.0.0.1:8000/api/v1/posts/
```

Получить определенный пост (GET):

```
http://127.0.0.1:8000/api/v1/posts/1/
```

Получить коментарии определенного поста (GET):

```
http://127.0.0.1:8000/api/v1/posts/1/comments/
```

Получить список всех групп (GET):

```
http://127.0.0.1:8000/api/v1/groups/
```

Создать новый пост (POST):

<sub>(Требуется аутентификация)<sub>
```
http://127.0.0.1:8000/api/v1/posts/
```