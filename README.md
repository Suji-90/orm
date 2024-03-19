# Ex02 Django ORM Web Application
## Date:19.03.24

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
<img width="576" alt="screen shot paint" src="https://github.com/Suji-90/orm/assets/150884148/592024c9-b3a4-49c3-8ae1-ffcabb41f19c">



## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
```
admin.py

from django.contrib import admin
from .models import Book_DB,Book_DBAdmin
admin.site.register(Book_DB,Book_DBAdmin)

models.py

from django.db import models
from django.contrib import admin
class Book_DB(models.Model):
      sno=models.IntegerField(primary_key="sno")
      name=models.CharField(max_length=50)
      author=models.CharField(max_length=70)
      price=models.IntegerField()
      publisher=models.CharField(max_length=60)

class Book_DBAdmin(admin.ModelAdmin):
    list_display=("sno","name","author","price","publisher")
```


## OUTPUT

<img width="956" alt="EXorm-1" src="https://github.com/Suji-90/orm/assets/150884148/a52ed6b7-c5ee-4148-abc6-e156e92126a9">


## RESULT
A Django application has been created that can be used to store and retrieve data from the database using Object Relational Mapping(ORM).
