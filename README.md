### Oписание
API для проекта yatube. Позволяет использовать проект на различных платформах.
В проект Yatube можно выкладывать посты, комментировать и следить за любимыми авторами с помошью пописки. 


### Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/impossible14/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python -m venv venv
```

```
source venv/Scripts/activate
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```


### Примеры
Некоторые примеры запросов к API

GET запрос к http://127.0.0.1:8000/api/v1/posts/ - отправит все посты

POST запрос к http://127.0.0.1:8000/api/v1/posts/ - создаст пост

```
{
"text": "ваш текст",
"image": "картинка",
"group": 0 (id группы)
}
```

GET запрос к http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/ - отправит все комментарии к определенному посту

POST запрос к http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/ - создает комментарий к определенному посту

```
{
  "text": "ваш комментарий"
}
```
