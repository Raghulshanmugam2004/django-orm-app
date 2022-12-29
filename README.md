# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![employee table](https://user-images.githubusercontent.com/119561118/209993276-376a3490-7ed9-4cdd-906c-ee3d89cdb5fe.png)
## DESIGN STEPS

### STEP 1:
Create a Django app
Go to the app directory
In models.py create two classes 
And save the models.py

### STEP 2:
Go to admins.py
And put the two class in admins.py from the models.py
And save the file


### STEP 3:
Start the Django server
Then move to admin page

Write your own steps

## PROGRAM

### File: Models.py
```python
from django.db import models
from django.contrib import admin

class Employee (models.Model):
    unique_number=models.CharField(max_length=20,primary_key=True)
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    job=models.CharField(max_length=100)

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('unique_number','name','age','email','job')
```


### File: Admin.py
```python
from django.contrib import admin
from .models import Employee,EmployeeAdmin

admin.site.register(Employee,EmployeeAdmin)
```
## OUTPUT
![employee new](https://user-images.githubusercontent.com/119561118/209993317-31440fa6-c62a-43b8-9ab7-738cc527866d.png)
###VERIFYING PRIMARY KEY
![primary key](https://user-images.githubusercontent.com/119561118/209993554-064c8b8b-360c-466f-bd62-0d4bf7b384a4.png)
## RESULT
The output for Django ORM is successful.
