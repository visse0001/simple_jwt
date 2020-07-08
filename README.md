# An app with a djangorestframework-simplejwt

## Development setup
Install Python 3.7.2

**Create a virtual environment:**

`python3 -m venv venv`

**Activate a venv:**

`source venv/bin/activate`

**Install dependencies:**

`pip install -r requirements.txt`

**Migrate db:**

`python3 manage.py makemigrations` <br/>
`python3 manage.py migrate`

**Create an admin account:**

`python manage.py createsuperuser`
## Access API
You may access API using Postman.

**e.g. access API:**
1. Create GET request for `http://127.0.0.1:8000/api/token/`

Expect:

`{
    "detail": "Method \"GET\" not allowed."
}`

Because it only accepts POST method.

2. First create a superuser, use command: 

`python manage.py createsuperuser`.

Remember your username and password.

But if you forgot anyway :) you could use this command 

`python manage.py changepassword <user_name>`

Create POST request for `http://127.0.0.1:8000/api/token/`, go to body section and select `raw` and the `JSON`.
In the body enter:

```
{
    "username": "your_username",
    "password": "your_password"
}
```

Expect refresh and access:
```
{
    "refresh": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTU5NDI4MzQ5MiwianRpIjoiYzBkNjUyY2JlNDk1NDE0YzlhYTVmMWMyY2QxMTdmZTEiLCJ1c2VyX2lkIjoxfQ._WmaX_q9Ejf7ZBryOFYJr7JfLRwNYoSOtT_YiU26Drc",
    "access": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNTk0MTk3MzkyLCJqdGkiOiJkMWIyMjA2OTY3MTY0NjA4YjYxNDk0MGEyYTQzMGVjNSIsInVzZXJfaWQiOjF9.OsxE0wGiQxWZqLBHx-b0IBOEWwzkJ6ng8u_Z1dGAzKw"
}
```

## Info

An app inspired from [tutorial](https://simpleisbetterthancomplex.com/tutorial/2018/12/19/how-to-use-jwt-authentication-with-django-rest-framework.html).