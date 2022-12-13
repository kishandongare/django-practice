# Django Concept:

# >> __init__.py

The folder which contain init.py file is considered as python package.

# >> def __str__()

To display an object in Django admin site and Thus you should always return a 
nice, human redable representational of the the model form the __str__() method 
write this method in your own model class which is inside model.py file.

from django.db import models

class Person(models.Model):

    first_name = models.CharField(max_length=50)
    
    last_name = models.CharField(max_length=50)
    
    def __str__(self):
    
        return "{} {}" .formate(self.first_name, self.last_name)
