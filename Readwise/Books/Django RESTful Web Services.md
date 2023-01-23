# Django RESTful Web Services

deck:: [[O'Reilly-Learning::Django RESTful Web Services]]\
author:: [[None]]\
full-title:: "Django RESTful Web Services"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/django-restful-web/9781788833929/ibis_generated_cover_thumbnail.jpg)
## Highlights
### Preface
### Defining the requirements for our first RESTful Web Service
- id:: 63c669f4-74d9-4dcc-a0cf-2e8f90af0aba
   What is REST? #flashcard 
    REST (short for Representational State Transfer) is the architectural style that has been driving modern and scalable web development recently.
-
- id:: 63c669f4-b2c0-4425-af37-f12e9965b900
   What does POST do with a toy? #flashcard 
    Create a new toy in the collection
-
### Creating a virtual environment with Python 3.x and PEP 405
- id:: 63c669f4-46c1-4133-a4ed-5e4a1baeb747
   What does PUT do with a toy? #flashcard 
    Update an existing toy
-
- id:: 63c669f4-89fa-4ed1-9c6e-b339bcdcc6fa
   Command to create a virtual environment in Linux: #flashcard 
    python3 -m venv ~/HillarDjangoREST/01
-
- id:: 63c669f4-d462-4b15-8350-41d7c6772388
   What does PUT do with a toy? #flashcard 
    Delete an existing toy
-
- id:: 63c669f4-09fd-4661-a8c9-873c92207863
   Command to make a virtual environment in PowerShell: #flashcard 
    python -m venv $env:userprofile\HillarDjangoREST\01
-
- id:: 63c669f4-553a-4c1b-9fcb-ffa951e60b5a
   About urls in DRF. #flashcard 
    In a RESTful Web Service, each resource has its own unique URL. In our web service, each toy will have its own unique URL.
-
### Activating the virtual environment
- id:: 63c669f4-f3c5-4ed7-ac3a-8df3c3e6bed7
   Steps to activate a virtual environment in PowerShell #flashcard 
    cd $env:USERPROFILE
     HillarDjangoREST\01\Scripts\Activate.ps1
-
- id:: 63c669f4-6c6d-4680-bf20-3fcaaa0b8679
   How do you start a virtual environment of Python in Linux? #flashcard 
    source ~/HillarDjangoREST/01/bin/activate
-
### Test your knowledge
### Deactivating the virtual environment
- id:: 63c669f4-1fbe-4764-b24a-90a408f824f8
   Which of the following commands creates a new app named books in Django? #flashcard 
    django startapp books
     python django.py startapp books
     python manage.py startapp books
-
- id:: 63c669f4-ff56-444a-b838-68bc07df4fdc
   How do you stop a virtual environment of Python in Linux? #flashcard 
    In macOS or Linux, just type deactivate and press Enter.
-
- id:: 63c669f4-6f45-4a85-9fda-91579b8dbc3e
   In Django, a subclass of which of the following classes represents a Django application and its configuration? #flashcard 
    django.apps.AppConfig
     django.application.configuration
     django.config.App
-
- id:: 63c669f4-aa9c-42dd-a0dc-cbfe38d4b0b7
   How do you stop a virtual environment of Python in Windows? #flashcard 
    In Windows PowerShell, you have to run the Deactivate.ps1 script in the Scripts folder.
-
### Understanding Django folders, files, and configurations
- id:: 63c669f4-436c-40f6-9206-55094f435f7e
   What does GET do with a toy? #flashcard 
    Retrieve a single toy
-
- id:: 63c669f4-d393-417d-8076-91085f9e92ac
   About names #flashcard 
    Now, we have to add toys.apps.ToysConfig as one of the installed apps in the restful01/settings.py file that configures settings for the restful01 Django project. I built the previous string by concatenating many values as follows: app name + .apps. + class name, which is, toys + .apps. + ToysConfig. In addition, we have to add the rest_framework app to make it possible for us to use Django REST framework.
-
- id:: 63c669f4-c549-4ecf-b852-416a2ffb1070
   URLs of lists VS details #flashcard 
    When we refer to a collection, we will use a slash (/) as the last character for the URL, as in http://localhost:8000/toys/. When we refer to a single resource of the collection we won't use a slash (/) as the last character for the URL, as in http://localhost:8000/toys/5
-
### Creating Django views combined with serializer classes
- id:: 63c669f4-5f6b-4640-8276-70588d470152
   About Response #flashcard 
    The JSONResponse class is a subclass of the django.http.HttpResponse class. The django.http.HttpResponse superclass represents an HTTP response with string content.
-
### Launching Django's development server
- id:: 63c669f4-a0b0-4b97-ab80-402d8f86514f
   Why 0 instead of localhost in DRF? #flashcard 
    If we specify 0.0.0.0 as the desired IP address for IPv4 configurations, the development server will listen on every interface on port 8000
-
### Understanding accepted and returned content types
- id:: 63c669f4-c328-401e-ba0f-e3177ce42376
   Which is the Response format type in DRF? #flashcard 
    No matter the value indicated for the Accept request header key, the response is always in the JSON format.
-