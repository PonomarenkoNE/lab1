# lab1
Лабораторна робота №1 з Технологія розробки Web-додатків


# Docker

To run project in docker simply run:

```sh
docker-compose up -d --build
```

And then to apply migrations:

```sh
docker-compose exec main-api /bin/sh -c "python manage.py makemigrations && python manage.py migrate"
```

Optionaly create superuser:

```sh
docker-compose exec main-api /bin/sh
python manage.py createsuperuser
<Ctrl + D>
```

To see logs:

```sh
docker-compose logs -f
```

# Run localy

Install requirements:

```sh
pip install -r requirements.txt
```

Apply migrations:

```sh
cd cuttly
```

```sh
python manage.py makemigrations
python manage.py migrate
```

Run server:

```sh
python manage.py runserver
```

Optionaly create superuser:

```sh
python manage.py createsuperuser
```