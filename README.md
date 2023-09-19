Yatube — это платформа для блогов, блог-сервис предполагает возможность зарегистрироваться, создать, отредактировать или удалить собственный пост, прокомментировать пост другого автора и подписаться на него.

Проект «API для Yatube»

Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:

git clone
cd api_final_yatube

Cоздать и активировать виртуальное окружение:

python3 -m venv env
source env/bin/activate

Установить зависимости из файла requirements.txt:

python3 -m pip install --upgrade pip
pip install -r requirements.txt

Выполнить миграции:

python3 manage.py migrate

Запустить проект:

python3 manage.py runserver

Пример POST-запроса с токеном Антона Чехова: добавление нового поста.
POST .../api/v1/posts/
{
    "text": "Вечером собрались в редакции «Русской мысли», чтобы поговорить о народном театре. Проект Шехтеля всем нравится.",
    "group": 1
}
Пример ответа:
{
    "id": 14,
    "text": "Вечером собрались в редакции «Русской мысли», чтобы поговорить о народном театре. Проект Шехтеля всем нравится.",
    "author": "anton",
    "image": null,
    "group": 1,
    "pub_date": "2021-06-01T08:47:11.084589Z"
}
