/ [Home](index.md)

# Wagtail

```

https://wagtail.org/

https://stackoverflow.com/questions/tagged/wagtail

https://github.com/danreeves/wagtailgmaps/tree/3.0.0

Bakery Demo:
https://github.com/wagtail/bakerydemo

docker-compose up --build



docker ps
CONTAINER ID   IMAGE            COMMAND                  CREATED          STATUS          PORTS                                       NAMES
17744007ad57   bakerydemo_app   "/code/docker-entryp…"   13 seconds ago   Up 12 seconds   0.0.0.0:8000->8000/tcp, :::8000->8000/tcp   bakerydemo_app_1
27f8ded08b6a   postgres:14.1    "docker-entrypoint.s…"   13 seconds ago   Up 13 seconds   5432/tcp                                    bakerydemo_db_1
6a3c81ae7f74   redis:6.2        "docker-entrypoint.s…"   13 seconds ago   Up 13 seconds   6379/tcp                                    bakerydemo_redis_1


docker-compose run app /venv/bin/python manage.py migrate
docker-compose run app /venv/bin/python manage.py load_initial_data

http://0.0.0.0:8000/


http://localhost:8000/admin/
admin / changeme

http://localhost:8000/admin/pages/84/view_draft/

https://madewithwagtail.org/

https://github.com/springload/awesome-wagtail

https://github.com/vicktornl/wagtail-stock-images

invoices
https://wagtailinvoices.readthedocs.io/en/latest/

https://django-salesman.readthedocs.io/en/latest/installation.html
```
