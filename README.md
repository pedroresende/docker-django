# Python Docker Compose environment

## How to start a new project

```
$ docker-compose build
$ docker-compose run python django-admin.py startproject composeexample .
$ docker-compose up -d
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

4. Add the following to the end of the file

```
STATIC_ROOT = '/code/static/'
```

5. Finally access to in your browser to `http://localhost:8000`
