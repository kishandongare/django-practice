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
class Meta:
        model = Movie
        fields = 'first_name', 'last_name'] #We can select model objects for form
```
or

```python
class Meta:
        model = Movie
        fields = '__all__' # we can select all field object from model
```
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
