# Django Concept:

# ``` __init__.py ```

The folder which contain init.py file is considered as python package.

# ``` def __str__()```

To display an object in Django admin site and Thus you should always return a 
nice, human redable representational of the the model form the __str__() method 
write this method in your own model class which is inside model.py file.

```python
from django.db import models
class Person(models.Model):
    first_name = models.CharField(max_length=50)
    last_name = models.CharField(max_length=50)
    def __str__(self):
          return "{} {}" .formate(self.first_name, self.last_name)
```

# Model Meta Sub class

https://www.geeksforgeeks.org/meta-class-in-models-django/

# Form Meta Sub Class

When we are making form field by using model field objects or The Meta class 
is used to change the behavior of the ModelForm. Within it, specify the model 
your fields come from and the fields you want to use from that model. 

```python

from django import forms
from .models import Movie 
# Create your forms here.

class MovieForm(forms.ModelForm):
         class Meta:
             model = Movie
             fields = ['first_name', 'last_name'] #We can select model objects for form
```

or

```python

from django import forms
from .models import Movie 
# Create your forms here.

class MovieForm(forms.ModelForm):
         class Meta:
             model = Movie
             fields = '__all__' # we can select all field object from model
```
        
 # Practice 
 https://ordinarycoders.com/blog/article/django-modelforms
 
 # Add model in django-admin
 
 After successfully create model then you have to add model in django admin
 
 ```python

admin.site.register(model class name)        
        
```
or if you want to show the field object in django admin interface the you 
have to write the following code

```python
from django.contrib import admin
from .models import Book
class BookAdmin(admin.ModelAdmin):
    list_display = ["title", "author", "published"]
admin.site.register(Book, BookAdmin)
```
or  you can use the (django.contrib.admin.register) decorator to register 
multiple models that using the same admin class.
        

```python
from django.contrib import admin
from .models import Track
@admin.register(Track)
class TrackAdmin(admin.ModelAdmin):
    list_display = ('title','artist')       
```
# DEBUG = True (settings.py)

This Django web application is running with debug mode turned on (DEBUG = True ). 
One of the main features of debug mode is the display of detailed error pages. 
If your app raises an exception when DEBUG is True, Django will display a detailed traceback, 
including a lot of metadata about your environment, such as all the currently defined Django 
settings (from settings.py).

Never deploy a site into production with DEBUG turned on. To disable debug mode, 
set DEBUG = False in your Django settings.py file.

# Media and Static File Setup(settings.py and urls.py)

1.STATIC_ROOT: 
STATIC_ROOT is just the path to the directory where static files have been collected.In
static/img
      /css
      /js
 
2.STATIC_URL:

STATIC_URL: It is simply the prefix of the URL that will be visible to 
the user while accessing the static files.

Example: Suppose a user tries to access a static file named "mystatic.txt" of the shop app. 
Then, he or she will access the file at http://127.0.0.1:8000/static/shop/mystatic.txt. 
 
3.MEDIA_ROOT: 

It is the path to the directory in which all the media files will be saved. 
Here, we have written(BASE_DIR, "media") which means that Django will create a 
folder named "media" under the base directory and all the media files will be 
saved in the "media" folder.

2.MEDIA_URL: 

Similar to the STATIC_URL, it is also the prefix of the URL that 
will be visible to the user while accessing the media files.


http://www.django.co.zw/en/tutorials/setting-django-s-static-and-media-urls/

# load crispy_forms_tags in django

https://ordinarycoders.com/blog/article/render-forms-with-django-crispy-forms
        
# Django crispy forms(Bootstrap)

https://ordinarycoders.com/blog/article/render-a-django-form-with-bootstrap
        
        
        
        
        
        
        
