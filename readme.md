
### Summary
It a simple Food ordering application using Django web Framework

## Running this project

To get this project up and running, should start by having Python installed on respective computer. It's advised to create a virtual environment to store  projects dependencies separately. You can install virtualenv with

```
pip install virtualenv
```

Clone or download this repository and open it in your editor of choice. In a terminal (mac/linux) or windows terminal, run the following command in the base directory of this project

```
virtualenv env
```

That will create a new folder `env` in project directory. Next activate it with this command on mac/linux:

```
source env/bin/active
```

Then install the project dependencies with

```
pip install -r requirements.txt
```

Now run the project with this command

```
python manage.py runserver
```

**Note** For deploying the application in server (production mode) refer this 
https://docs.djangoproject.com/en/3.1/howto/deployment/

---

## Database Configuration
Now Create a Postgress Db And link with the Django ORM

By default, Django is configured to use SQLite as its backend.

To use Postgres instead, “settings.py” needs to be updated:

---

DATABASES = {
    
    'default': {

        'ENGINE': 'django.db.backends.postgresql_psycopg2',

        'NAME': ‘<db_name>’,

        'USER': '<db_username>',

        'PASSWORD': '<password>',

        'HOST': '<db_hostname_or_ip>',

        'PORT': '<db_port>',

    }

}

---

Now build the default schema.Django was designed with user access in mind, so by default a Django application will create a database schema involving users, groups, and permissions. To create the schema, generate a migration and run it:


```
python manage.py makemigrations

python manage.py migrate

```

After creating the default schema, create the default superuser:

```
python manage.py createsuperuser

```
process look like this;
```
Email address: xxxxxxx@gmail.com

Password: 

Password (again): 

Superuser created successfully.
```

-----------------------------
