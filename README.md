# An app with a djangorestframework-simplejwt

## Development setup
Install Python 3.7.2

## Create a virtual environment:
`python3 -m venv venv`

## To activate a venv:
`source venv/bin/activate`

## Install dependencies:
`pip install -r requirements.txt`

## Migrate db:
`python3 manage.py makemigrations` <br/>
`python3 manage.py migrate`

## To create an admin account:
`python manage.py createsuperuser`

## Info

App inspired from [tutorial](https://simpleisbetterthancomplex.com/tutorial/2018/12/19/how-to-use-jwt-authentication-with-django-rest-framework.html)