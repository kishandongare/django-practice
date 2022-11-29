# Django Practice

1) Django is a Python-based web framework that allows us to quickly create efficient web applications.

2) Django provides built-in features for everything including Django Admin Interface, default database SQLlite3, etc. 

3) When we are building a website, we always need a similar set of components: a way to handle user authentication (signing up, signing in, signing out), a management panel for our website django admin.

# Why Django Framework ?

1) Easy Framework to learn, Excellent documentation, high scalability and rapid development.

2) Python has huge library set and features such as Web Scrapping, Machine Learning, Image Processing, Scientific Computing, etc. One can integrate it all this with web application and do lots and lots of advance stuff.

3) Used by Top MNCs and Companies, such as Instagram, Disqus, Spotify, Youtube, Bitbucket, Dropbox, etc. and the list is never-ending.


# MVT Pattern
Django, a Python framework to create web applications, is based on Model-View-Template (MVT) architecture. MVT is a software design pattern for developing a web application. It consists of the following three entities:

1)Model

2)View

3)Template

# Model
A Model is an object that defines the structure of the data in the Django application.

It is responsible for maintaining the entire application’s data for which it provides 
various mechanisms to add, update, read and delete the data in the database.

# View
A View is a handler function that accepts HTTP requests, processes them, and returns the HTTP response.

It retrieves the necessary data to fulfill the request using Models and renders them on the user interface using Templates.

It can also create an HTML page using an HTML template dynamically, and populate it with data fetched from the model.

# Template

A Template is a text file that defines the structure or layout of the user interface. 
The text file can be any type of file; for example HTML, XML, etc.

Control flow in MVT architecture
![image](https://user-images.githubusercontent.com/66677660/204590322-df26fef4-96d0-45b9-bf6b-1b79909c2dce.png)

>> The user interacts with a Django application using a URL that is passed to the MVT architecture. 
>> A URL mapper is used to redirect the requests to the appropriate view based on the request URL.
>> If an appropriate view is found, it will be invoked.
>> The View will interact with the Model and retrieve the necessary data from the database via Model.
>> The View will render an appropriate template along with the retrieved data to the user.

# Installation of Django
https://www.geeksforgeeks.org/django-introduction-and-installation/
>window
https://docs.djangoproject.com/en/3.2/howto/windows/

>ubuntu
https://www.digitalocean.com/community/tutorials/how-to-install-the-django-web-framework-on-ubuntu-18-04


# Ubuntu installation Django(terminal)

> kishan@kishan25:~$ python -V

> Python 2.7.18

> kishan@kishan25:~$ python3 -V

> Python 3.8.10

> kishan@kishan25:~$ ls

> kishan@kishan25:~$ cd django

> kishan@kishan25:~/django$ sudo apt install python3-virtualenv

> kishan@kishan25:~/django$ virtualenv venv

> kishan@kishan25:~/django$ . venv/bin/activate

> (venv) kishan@kishan25:~/django$ pip install django

> (venv) kishan@kishan25:~/django$ django-admin startproject crudexample 

> (venv) kishan@kishan25:~/django$ ls

> crudexample  venv

> (venv) kishan@kishan25:~/django$ cd crudexample

> (venv) kishan@kishan25:~/django/crudexample$ python3 manage.py startapp employee

> (venv) kishan@kishan25:~/django/crudexample$ ls 

> crudexample employee  manage.py

> (venv) kishan@kishan25:~/django/crudexample$ python3 manage.py runserver

November 02, 2021 - 17:01:58
Django version 3.2.9, using settings 'crudexample.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.


# Django Project Structure

![image](https://user-images.githubusercontent.com/66677660/184409295-da6a4e5d-8de4-4ac5-9a93-37b0cf07db52.png)

# pycharm setup
create new project and virtual environment (first is project name and venv folder) in 
Terminal:

> (venv) kishan@kishan25:~/myapp$ pip install django

> (venv) kishan@kishan25:~/myapp$  django-admin startproject crudexample

>  (venv) kishan@kishan25:~/myapp$ cd crudexample

> (venv) kishan@kishan25:~/myapp/crudexample$ django-admin startapp crud

> (venv) kishan@kishan25:~/myapp/crudexample$ python manage.py runserver

>
November 03, 2021 - 06:31:59
Django version 3.2.9, using settings 'main.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
> 

# intro to django

https://www.djangoproject.com/start/

# creating project

https://www.tutorialspoint.com/django/django_creating_project.htm

# makemigration vs Migrates

https://www.javatpoint.com/django-database-migrations

# Django render()
https://www.educative.io/answers/how-to-render-data-in-django

# gunicorn
Gunicorn is detailed as "A Python WSGI HTTP Server for UNIX".
Gunicorn is a WSGI server and we can run any web application using Gunicorn if it supports WSGI. 
So, you can run not only your Django application, but you can also run, for example, Flask application 
using Gunicorn because it also supports WSGI.

WSGI is a protocol, it’s a standard of communication between a web server and a web application. 
Basically, between Gunicorn and Flask or Django. The web server should know how to speak to the 
web application, and the web application should know how to respond to the web server. They both 
should talk using the same language. And the language is WSGI

https://docs.djangoproject.com/en/4.1/howto/deployment/wsgi/gunicorn/

![image](https://user-images.githubusercontent.com/66677660/204316995-0c90a492-c6e2-4cd1-bbac-90e08050ac5e.png)
![image](https://user-images.githubusercontent.com/66677660/204318928-4171d286-29ec-49cd-9cee-f0db550c12bb.png)

# WSGI(Web Server Gateway Interface)
> The Web Server Gateway Interface (WSGI) is a standard interface between web server software 
> and web applications written in Python.

https://www.liquidweb.com/kb/what-is-wsgi/

# Nginx

NGINX doesn't “know” how to run Python, so it needs a gateway to an environment that does.a more popular choice
for communication between Python and NGINX is the Web Server Gateway Interface (WSGI)

Nginx is a web server. It serves static files, however it cannot execute and host Python application.So,
you need gateway between nginx and python where WSGI is an option. So, you mean, there must be at 
least one WSGI compatible application server such as uWSGI or Gunicorn to run python web application with WSGI?

Nginx is a web server that can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache.

concept of reverse proxy
https://www.cloudflare.com/en-gb/learning/cdn/glossary/reverse-proxy/

![image](https://user-images.githubusercontent.com/66677660/204323833-6f52b2f7-8b4b-4125-bca6-dff8d54f6f1b.png)

>>Reverse Proxy

![image](https://user-images.githubusercontent.com/66677660/204323724-b389b348-38be-49d8-8b26-215baf66fee9.png)


