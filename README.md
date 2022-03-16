# Yatube API
### Описание
Реализация API для социальной сети Yatube

API может:
- аутентифицироваться по токену;
- создавать/редактировать/удалять посты;
- создавать/редактировать/удалять/ комментарии;
- подписываться на автора;

### Технологии
- Python 3.8
- Django 2.2.19
- DRF 3.12.4
- simplejwt 4.7.2

### Примеры запросов к API
```
- GET api/v1/posts/ - список постов с пагинацией;
- GET api/v1/posts/{id}/ - пост по id;
- GET api/v1/groups/ - список групп;
- GET api/v1/groups/{id}/ - группа по id;
- GET api/v1/{post_id}/comments/ - комментарии к посту;
- GET api/v1/{post_id}/comments/{id}/ - комментарий к посту по id.
```
### Запуск проекта в dev-режиме
- Установите и активируйте виртуальное окружение
- Установите зависимости из файла requirements.txt
```
pip install -r requirements.txt
```
- Создаём и делаем миграции:
```
python manage.py makemigrations и python manage.py migrate
``` 
- В папке с файлом manage.py выполните команду:
```
python3 manage.py runserver
```
### Авторы
Стасян