![](https://img.shields.io/badge/Python-3.8-blue) 
![](https://img.shields.io/badge/Django-2.2.19-green)
![](https://img.shields.io/badge/DjangoRestFramework-3.12.4-green)
![](https://img.shields.io/badge/SimpleJWT-yellow)
![](https://img.shields.io/badge/SQLite-red)


# Yatube API

## Описание
Реализация API для социальной сети Yatube

API может:
- аутентифицироваться по токену;
- создавать/редактировать/удалять посты;
- создавать/редактировать/удалять/ комментарии;
- подписываться на автора;

## Документация проекта
```
http://localhost:8000/redoc/
```

## Примеры запросов к API
```
- GET api/v1/posts/ - список постов с пагинацией;
- GET api/v1/posts/{id}/ - пост по id;
- GET api/v1/groups/ - список групп;
- GET api/v1/groups/{id}/ - группа по id;
- GET api/v1/{post_id}/comments/ - комментарии к посту;
- GET api/v1/{post_id}/comments/{id}/ - комментарий к посту по id.
```

## Доступные API запросы
метод                                            | GET | POST | PUT | PATCH | DEL |
-------------------------------------------------|-----|------|-----|-------|-----|
/api/v1/token/ | - | V | - | - | - |
/api/v1/token/refresh/ | - | V | - | - | - |
/api/v1/posts/  | V | V | - | - | - |
/api/v1/posts/{id}/ | V | - | V | V | V |
/api/v1/posts/{post_id}/comments/ | V | V | - | - | - |
/api/v1/posts/{post_id}/comments/{comment_id}/ | V | - | V | V | V |
/api/v1/follow/ | V | V | - | - | - |
/api/v1/group/ | V | V | - | - | - |

---

## Запуск проекта в dev-режиме
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

## Авторы
[Шалгынов Станислав](https://github.com/stasrls)

## Лицензия
The Unlicense
