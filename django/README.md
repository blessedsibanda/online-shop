# Online Shop

## E-Commerce website using django

### Instructions

---

- create & activate virtual environment

```
python3 -m venv venv

source venv/bin/activate
```

- Install pip dependencies

```
(venv) pip install -r requirements.txt
```

- Run database migrations

```
(venv) python manage.py migrate
```

- Run development server

```
(venv) python manage.py runserver
```

Open browser at http://127.0.0.1:8000 to view the app

- Open a new terminal (with same working directory), activate virtual environment and run celery (make sure redis is running)

```
(venv) celery -A online_shop worker -l info
```

- Open another terminal (with same working directory), activate virtual environment and run flower (to monitor celery)

```
(venv) celery -A online_shop flower
```

Open browser at http://127.0.0.1:5555 to view the flower dashboard
