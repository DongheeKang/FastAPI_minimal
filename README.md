# fastapi-example [![CircleCI](https://circleci.com/gh/marciovrl/fastapi-example.svg?style=svg)](https://circleci.com/gh/marciovrl/fastapi-example)

A simple example of using Fast API in Python.

## Preconditions:

- Python 3.8.1

## Clone the project

```
git clone https://github.com/DongheeKang/Fastapi_minimal.git
```

## Run local

### Install dependencies

```
pip install -r requirements.txt
```

### Run server
Uvicorn is an ASGI web server implementation for deployment with python
Typically you should run uvicorn from the command line.
```
uvicorn app.main:app --reload
```

### Run test

```
pytest app/test.py
```

## Run with docker

### Run server

```
docker-compose up -d --build
```

### Run test

```
docker-compose exec app pytest test/test.py
```

## API documentation (provided by Swagger UI)

```
http://127.0.0.1:8000/docs
```

### Run server with postgres

```
docker-compose exec db psql --username=fastapi --dbname=fastapi_dev
```

### Continuous Integration is implemented by circleCI 
If you want to use github actions for build in CI, there is an easy step to migrate from circleci to github actions. 
https://docs.github.com/en/actions/migrating-to-github-actions/migrating-from-circleci-to-github-actions
