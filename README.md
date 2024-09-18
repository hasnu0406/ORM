# Ex02 Django ORM Web Application
## Date: 18.09.2024

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

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
Models.py 
from django.db import models
from django.contrib import admin
# Create your models here.

class Bank(models.Model):
    customer_id = models.IntegerField(primary_key=True)
    customer_name = models.CharField(max_length=50)
    account_type = models.CharField(max_length=50)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)  
    monthly_interest = models.DecimalField(max_digits=5, decimal_places=2)  
    due_date = models.DateField()

class Loandetails(admin.ModelAdmin):
    list_display= ('customer_id','customer_name','account_type','loan_amount','monthly_interest','due_date')

admin.py 
from django.contrib import admin
from .models import Bank,Loandetails

# Register your models here.
admin.site.register(Bank,Loandetails)
```
## OUTPUT

Include the screenshot of your admin page.
![Image3](https://github.com/user-attachments/assets/9bd2aa9a-f30c-4b9f-b008-a3429706de01)
![image4](https://github.com/user-attachments/assets/4352920e-4883-48f0-a731-9b221fb3848a)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
