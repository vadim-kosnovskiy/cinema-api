# Cinema API

API service for cinema management written on DRF

### Installing using GitHub

Install PostgresSQL and create db

```
git clone https://github.com/vadim-kosnovskiy/docker-cinema.git
cd cinema_API
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
set POSTGRES_HOST=<your db hostname>
set POSTGRES_DB=<your db name>
set POSTGRES_USER=<your db user>
set POSTGRES_PASSWORD=<your db password>
set SECRET_KEY=<your secret key>
python manage.py migrate
python manage.py runserver
```
### Run with docker

Docker should be installed
```
docker-compose build
docker-compose up
```

### Getting access

- create user via /api/user/register/
- get access token via /api/user/token/

## Features

- JWT authentication
- Admin panel /admin/
- Documentation is located at /api/doc/swagger/ or /api/doc/redoc/
- Managing orders and tickets
- Creating movies with genres and actors
- Creating cinema halls
- Adding movie sessions