# Blog CRUD Django App - with MYSQL

## Introduction
This guide will walk you through building a basic CRUD (Create, Read, Update, Delete) application using Django, a high-level Python web framework, and integrating it with a MySQL database.

## Prerequisites
- Basic understanding of Python programming language.
- Familiarity with Django framework.
- Python installed on your machine.
- MySQL installed on your machine.

## Steps

1. **Setup Django Project:**
   - Install Django using pip:
     ```
     pip install django
     ```
   - Create a new Django project:
     ```
     django-admin startproject myproject
     ```
   - Navigate into the project directory:
     ```
     cd myproject
     ```

2. **Create Django App:**
   - Create a new Django app within the project:
     ```
     python manage.py startapp myapp
     ```

3. **Define Models:**
   - Define your models in `models.py` file within the app directory (`myapp/models.py`).

4. **Create Views:**
   - Define views to handle CRUD operations in `views.py` file within the app directory (`myapp/views.py`).

5. **Setup URLs:**
   - Configure URL patterns to route requests to appropriate views in `urls.py` file within the app directory (`myapp/urls.py`).

6. **Create Templates:**
   - Create HTML templates to render views in the `templates` directory within the app directory (`myapp/templates`).

7. **Run Migrations:**
   - Apply migrations to create database tables:
     ```
     python manage.py makemigrations
     python manage.py migrate
     ```

8. **Run Development Server:**
   - Start the Django development server:
     ```
     python manage.py runserver
     ```

## How to Add MySQL Database to Django

1. **Install MySQL Client:**
   - Install MySQL Client for Python using pip:
     ```
     pip install mysqlclient
     ```

2. **Configure Database Settings:**
   - Open `settings.py` file in your Django project (`myproject/settings.py`).
   - Update the `DATABASES` setting to use MySQL:
     ```python
     DATABASES = {
         'default': {
             'ENGINE': 'django.db.backends.mysql',
             'NAME': 'your_database_name',
             'USER': 'your_mysql_username',
             'PASSWORD': 'your_mysql_password',
             'HOST': 'localhost',
             'PORT': '3306',
         }
     }
     ```
     Replace `'your_database_name'`, `'your_mysql_username'`, and `'your_mysql_password'` with your MySQL database name, username, and password respectively.

3. **Create MySQL Database:**
   - Create a new MySQL database with the specified name if it doesn't exist:
     ```sql
     CREATE DATABASE your_database_name CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
     ```

4. **Run Migrations:**
   - Apply migrations to create database tables:
     ```
     python manage.py makemigrations
     python manage.py migrate
     ```

5. **Run Development Server:**
   - Start the Django development server:
     ```
     python manage.py runserver
     ```

## Conclusion
Congratulations! You have successfully integrated a MySQL database with your Django application using MySQL Client. You can now utilize the power of MySQL for storing and managing your application's data.

## Additional Resources
- [Django Documentation](https://docs.djangoproject.com/en/stable/)
- [Django Models Documentation](https://docs.djangoproject.com/en/stable/topics/db/models/)
- [Django Views Documentation](https://docs.djangoproject.com/en/stable/topics/http/views/)
- [Django Templates Documentation](https://docs.djangoproject.com/en/stable/topics/templates/)
- [MySQL Documentation](https://dev.mysql.com/doc/)
