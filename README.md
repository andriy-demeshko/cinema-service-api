# CineTicket API

API service for cinema management written on DRF

## Installing using GitHub

Install PostgresSQL and create db

```shell
git clone https://github.com/andriy-demeshko/cinema-service-api.git
cd py-dockerize-cinema
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt

create file .env with vars:  # Set Environment Variables like in file .env.sample
DJANGO_SECRET_KEY=<your Django secret key>
POSTGRES_HOST=<your db hostname>
POSTGRES_NAME=<your db name>
POSTGRES_USER=<your db username>
POSTGRES_PASSWORD=<your db user password>

python manage.py migrate
python manage.py runserver  # starts Django server
```

## Run with Docker

Docker should be installed

```shell
docker-compose build
docker-compose up
```

## Getting access

* create user via /api/user/register/
* get access token via /api/user/token/
