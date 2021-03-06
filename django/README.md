# Django-starter-kit

Django Starter Kit

## Description

yoshikawa/django-starter-kit − learning about Django REST framework

### requirements

|Lang/FrameWork|Version|
|:--|--:|
|Python|3.8.5|
|Django|3.1|
|Django REST framework|3.11.1|

Please check it! [Django REST framework](https://github.com/encode/django-rest-framework)

## Usage

Install using `pip`.

```sh
pip install django
pip install djangorestframework
```

Add 'rest_framework' to your INSTALLED_APPS setting.(**We have already set.**)

```python
INSTALLED_APPS = [
    ...
    'rest_framework',
]
```

### Backend Server

```sh
./manage.py runserver
```

You can now open the API in your browser at `http://127.0.0.1:8000/`, and view your new 'users' API. If you use the `Login` control in the top right corner you'll also be able to add, create and delete users from the system.

You can also interact with the API using command line tools such as [`curl`](https://curl.haxx.se/). For example, to list the users endpoint:

```sh
$ curl -H 'Accept: application/json; indent=4' -u admin:password http://127.0.0.1:8000/users/
[
    {
        "url": "http://127.0.0.1:8000/users/1/",
        "username": "admin",
        "email": "admin@example.com",
        "is_staff": true,
    }
]
```

Or to create a new user:

```sh
$ curl -X POST -d username=new -d email=new@example.com -d is_staff=false -H 'Accept: application/json; indent=4' -u admin:password http://127.0.0.1:8000/users/
{
    "url": "http://127.0.0.1:8000/users/2/",
    "username": "new",
    "email": "new@example.com",
    "is_staff": false,
}
```

## Contribution

1. [Fork it](https://github.com/yoshikawa/django-starter-kit/fork)
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. reate new Pull Request

## Licence

[WTFPL](https://github.com/yoshikawa/django-starter-kit/blob/master/LICENSE)

## Author

[Yoshikawa Taiki](https://github.com/yoshikawa)