# Python Docker Compose environment

## How to start a new project

```
$ docker-compose build
$ docker-compose run web django-admin.py startproject composeexample .
```

### Database Configuration

1. In your project directory, edit the composeexample/settings.py file.

2. Replace the DATABASES = ... with the following:

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'postgres',
        'USER': 'postgres',
        'HOST': 'db',
        'PORT': 5432,
    }
}
```

