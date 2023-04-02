```
## Описание проекта:
```
Проект *API Yatube* - это *API* для проектра *Yatube*, только без фронтенда и view-функции приложения posts.

С помощью *API Yatube* можно запрашивать данные о постах, группах, комментариях в социальной сети *Yatube*, а также создавать новые.

*Yatube*- это учебный проект курса "Python-разработчик" от Яндекс-Практикума, который представляет собой социальную сеть с возможностью публикации постов и подписки на авторов.

Автор: Гараев Фархад
```
## Как запустить проект:
```
Клонировать репозиторий и перейти в него в командной строке:
```
'git clone git@github.com:PARTYNEXTDOORS/api_final_yatube.git'
```
'cd api_final_yatube'
```
Cоздать и активировать виртуальное окружение:
```
'python -m venv venv'
```
'source venv/Scripts/activate'
```
Установить зависимости из файла requirements.txt:
```
'python -m pip install --upgrade pip'
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
```
## Примеры запросов к API:
```
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