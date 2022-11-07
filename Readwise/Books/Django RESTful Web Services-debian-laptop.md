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
- id:: 63639918-605a-4559-90c4-58ed1145f31d
   What is REST? #flashcard 
    REST (short for Representational State Transfer) is the architectural style that has been driving modern and scalable web development recently.
-
- id:: 63639918-3c07-42cb-a89f-554ff5984d94
   What does POST do with a toy? #flashcard 
    Create a new toy in the collection
-
### Creating a virtual environment with Python 3.x and PEP 405
- id:: 63639918-b4e6-434b-be7c-ffe6c4204793
   What does PUT do with a toy? #flashcard 
    Update an existing toy
-
- id:: 63639918-9ccd-4452-80aa-f0ca465f424f
   Command to create a virtual environment in Linux: #flashcard 
    python3 -m venv ~/HillarDjangoREST/01
-
- id:: 63639918-8d3c-40a3-99e6-366fefac40d3
   What does PUT do with a toy? #flashcard 
    Delete an existing toy
-
- id:: 63639918-aae8-4064-a3b3-74f93947fc36
   Command to make a virtual environment in PowerShell: #flashcard 
    python -m venv $env:userprofile\HillarDjangoREST\01
-
- id:: 63639918-3de6-4d40-8e11-f2093cf02123
   About urls in DRF. #flashcard 
    In a RESTful Web Service, each resource has its own unique URL. In our web service, each toy will have its own unique URL.
-
### Activating the virtual environment
- id:: 63639918-ddb8-4774-a52d-0286cbac2c12
   Steps to activate a virtual environment in PowerShell #flashcard 
    cd $env:USERPROFILE
     HillarDjangoREST\01\Scripts\Activate.ps1
-
- id:: 63639918-ebef-4ef1-8bee-74a4627b5042
   How do you start a virtual environment of Python in Linux? #flashcard 
    source ~/HillarDjangoREST/01/bin/activate
-
### Test your knowledge
### Deactivating the virtual environment
- id:: 63639918-3925-4447-86a1-fbe41c0be7e5
   Which of the following commands creates a new app named books in Django? #flashcard 
    django startapp books
     python django.py startapp books
     python manage.py startapp books
-
- id:: 63639918-880a-4e6b-84a3-7eafc0257c46
   How do you stop a virtual environment of Python in Linux? #flashcard 
    In macOS or Linux, just type deactivate and press Enter.
-
- id:: 63639918-b939-4701-91af-b15447c82e55
   In Django, a subclass of which of the following classes represents a Django application and its configuration? #flashcard 
    django.apps.AppConfig
     django.application.configuration
     django.config.App
-
- id:: 63639918-b5a8-48df-b91f-2fd8c64d2b97
   How do you stop a virtual environment of Python in Windows? #flashcard 
    In Windows PowerShell, you have to run the Deactivate.ps1 script in the Scripts folder.
-
### Understanding Django folders, files, and configurations
- id:: 63639918-6d1c-4856-96ca-c438b51122bc
   What does GET do with a toy? #flashcard 
    Retrieve a single toy
-
- id:: 63639918-af14-4466-80c1-61c413f8584c
   About names #flashcard 
    Now, we have to add toys.apps.ToysConfig as one of the installed apps in the restful01/settings.py file that configures settings for the restful01 Django project. I built the previous string by concatenating many values as follows: app name + .apps. + class name, which is, toys + .apps. + ToysConfig. In addition, we have to add the rest_framework app to make it possible for us to use Django REST framework.
-
- id:: 63639918-0c39-4b34-abf2-9f4c55bb31b2
   URLs of lists VS details #flashcard 
    When we refer to a collection, we will use a slash (/) as the last character for the URL, as in http://localhost:8000/toys/. When we refer to a single resource of the collection we won't use a slash (/) as the last character for the URL, as in http://localhost:8000/toys/5
-
### Creating Django views combined with serializer classes
- id:: 63639918-a409-4dae-aeb7-0cf3b695fb51
   About Response #flashcard 
    The JSONResponse class is a subclass of the django.http.HttpResponse class. The django.http.HttpResponse superclass represents an HTTP response with string content.
-
### Launching Django's development server
- id:: 63639918-fba8-4b50-8f13-63e79c6109fb
   Why 0 instead of localhost in DRF? #flashcard 
    If we specify 0.0.0.0 as the desired IP address for IPv4 configurations, the development server will listen on every interface on port 8000
-
### Understanding accepted and returned content types
- id:: 63639918-a754-4ff6-8c4a-8a154ed1a514
   Which is the Response format type in DRF? #flashcard 
    No matter the value indicated for the Accept request header key, the response is always in the JSON format.
-