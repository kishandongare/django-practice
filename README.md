# Django Practice
Django is a Python-based web framework that allows you to quickly create efficient web applications. It is also called batteries included framework because Django provides built-in features for everything including Django Admin Interface, default database SQLlite3, etc. 

When you’re building a website, you always need a similar set of components: a way to handle user authentication (signing up, signing in, signing out), a management panel for your website, forms, a way to upload files, etc. Django gives you ready-made components to use and that too for rapid development.

# Why Django Framework ?
1.Excellent documentation and high scalability.

2.Used by Top MNCs and Companies, such as Instagram, Disqus, Spotify, Youtube, Bitbucket, Dropbox, etc. and the list is never-ending.

3.Easiest Framework to learn, rapid development and Batteries fully included.

4.The last but not least reason to learn Django is Python, Python has huge library and features such as Web Scrapping, Machine Learning, Image Processing, Scientific Computing, etc. One can integrate it all this with web application and do lots and lots of advance stuff.

# MVC Pattern
Model View Controller or MVC as it is popularly called, is a software design pattern for developing web applications. A Model View Controller pattern is made up of the following three parts −

Model − The lowest level of the pattern which is responsible for maintaining data.

View − This is responsible for displaying all or a portion of the data to the user.

Controller − Software Code that controls the interactions between the Model and View.

MVC is popular as it isolates the application logic from the user interface layer and supports separation of concerns. Here the Controller receives all requests for the application and then works with the Model to prepare any data needed by the View. The View then uses the data prepared by the Controller to generate a final presentable response. The MVC abstraction can be graphically represented as follows.
![image](https://user-images.githubusercontent.com/66677660/138484939-ef9ca7ce-e14a-40d3-887b-88aa71aad54d.png)
>The Model
The model is responsible for managing the data of the application. It responds to the request from the view and it also responds to instructions from the controller to update itself.

>The View
It means presentation of data in a particular format, triggered by a controller's decision to present the data. They are script-based templating systems like JSP, ASP, PHP and very easy to integrate with AJAX technology.

>The Controller
The controller is responsible for responding to the user input and perform interactions on the data model objects. The controller receives the input, it validates the input and then performs the business operation that modifies the state of the data model.

Struts2 is a MVC based framework.

# MVT Pattern

The Model-View-Template (MVT) is slightly different from MVC. In fact the main difference between the two patterns is that Django itself takes care of the Controller part (Software Code that controls the interactions between the Model and View), leaving us with the template. The template is a HTML file mixed with Django Template Language (DTL).

The following diagram illustrates how each of the components of the MVT pattern interacts with each other to serve a user request −
![image](https://user-images.githubusercontent.com/66677660/138485489-395d1a7b-badd-4ecc-96cb-040e26b6beaa.png)

The developer provides the Model, the view and the template then just maps it to a URL and Django does the magic to serve it to the user.

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

# WSGI(Web Server Gateway Interface)
https://www.liquidweb.com/kb/what-is-wsgi/
