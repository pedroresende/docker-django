# Python Docker Compose environment

## How to start a new project

```
$ docker-compose build
$ docker-compose run python django-admin.py startproject composeexample .
```

### Database Configuration

1. In your project directory, edit the composeexample/settings.py file.

2. Replace the ALLOWED_HOSTS by

```
ALLOWED_HOSTS = ['*']
```

in order to allow connections from the guest O.S.

3. Replace the DATABASES = ... with the following:

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'django',
        'USER': 'root',
        'PASSWORD': 'django',
        'HOST': 'db',
        'PORT': 3306,
    }
}
```

