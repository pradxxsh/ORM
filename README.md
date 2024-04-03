# Ex02 Django ORM Web Application
## Date: 01/03/2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram


![orm1](https://github.com/pradxxsh/ORM/assets/131758539/3a50b18f-3d4f-4fec-ab34-6a24dd4f052f)


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
models.py
from django.db import models
from django.contrib import admin
class Book(models.Model):
   book_id=models.IntegerField(primary_key=True);
   book_name=models.CharField(max_length=20);
   price=models.IntegerField();
   author_name=models.CharField(max_length=50);
   author_email=models.EmailField();
class BookAdmin(admin.ModelAdmin):
  list_display=("book_id","book_name","price","author_name","author_email");

admin.py

from django.contrib import admin
from .models import book,bookAdmin
admin.site.register(book,bookAdmin)
```

## OUTPUT

![orm2](https://github.com/pradxxsh/ORM/assets/131758539/6015d9e6-5a2a-4c06-a191-afd8b8ffe552)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
