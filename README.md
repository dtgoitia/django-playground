# Observations

The following notes were taken while following the _Django REST Framework_ quickstart tutorial[^1].

## Installation

### 1 Set Git and Pipenv

```shell
git init
git config user.email "david.torralba.goitia@gmail.com"
git remote add origin git@github.com:dtgoitia/django-playground.git

pipenv install --python 3.7
pipenv install --dev "flake8"
pipenv install django
pipenv install djangorestframework
```

### 2 Start project

```shell
$ pipenv run django-admin.py startproject tutorial .
$ cd tutorial
$ pipenv run django-admin.py startapp quickstart
$ cd ..
```

In windows requires to call straight away the file as such [^2]:

```shell
$ pipenv run python C:\\Users\\david-torralba-goiti\\.virtualenvs\\djangoplayground-4loSAOGh\\Scripts\\django-admin.py startproject tutorial .
$ cd tutorial
$ pipenv run python C:\\Users\\david-torralba-goiti\\.virtualenvs\\djangoplayground-4loSAOGh\\Scripts\\django-admin.py startapp quickstart
$ cd ..
```

### 3 Sync database for first time

```shell
$ pipenv run python manage.py migrate
```

### 4 Create super user

```bash
$ pipenv run python manage.py createsuperuser --email admin@example.com --username admin
```

For the purpose of this test, the password is `1234`.

[^1]: http://www.django-rest-framework.org/tutorial/quickstart/
[^2]: https://stackoverflow.com/questions/3681216/django-admin-py-startproject-is-not-working