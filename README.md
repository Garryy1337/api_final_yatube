api_final_yatube
Описание:
Финальная часть учебного проекта социальной сети, в которой есть возможность публиковать записи, комментировать их и подписываться/отписываться от авторов.

Технологии:
Python 3.7, Django 2.2, DRF, JWT

Как запустить проект:
Клонируй репозиторий и перейди в него в командной строке:

 cd api_final_yatube

Cоздай и активируй виртуальное окружение:

python3 -m venv venv

Если у тебя Linux/macOS

source venv/bin/activate

Если у тебя windows

source env/scripts/activate

python3 -m pip install --upgrade pip

Установи зависимости из файла requirements.txt:

pip install -r requirements.txt

Выполни миграции:

python3 manage.py migrate

Запусти проект:

python3 manage.py runserver


Примеры запросов к API:
POST-запрос на эндпоинт api/v1/posts/:

{
    "text": "string",
    "image": "string",
    "group": 1
}
Ответ:

{
    "id": 1,
    "author": "username",
    "text": "string",
    "pub_date": "2022-03-13T14:15:22Z",
    "image": "string",
    "group": 1
}
GET-запрос на эндпоинт api/v1/posts/{post_id}/comments/ вернет список комментариев к посту:

[
    {
        "id": 1,
        "author": "username",
        "text": "string",
        "created": "2022-03-13T14:15:22Z",
        "post": 1
    },
    {
        "id": 2,
        "author": "username",
        "text": "string",
        "created": "2022-03-13T14:15:22Z",
        "post": 1
    }
]
Документация к API доступна по ссылке http://127.0.0.1:8000/redoc/ после запуска сервера разработчика
