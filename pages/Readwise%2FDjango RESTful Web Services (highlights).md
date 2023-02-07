title:: Readwise/Django RESTful Web Services (highlights)
deck:: [[O'Reilly-Learning::Django RESTful Web Services]]
author:: [[]]
full-title:: "Django RESTful Web Services"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Tuesday, 07-02-2023]]
	- Preface
	- Defining the requirements for our first RESTful Web Service
		- -
			- What is REST? #flashcard
				- REST (short for Representational State Transfer) is the architectural style that has been driving modern and scalable web development recently.
		- -
		- -
			- What does POST do with a toy? #flashcard
				- Create a new toy in the collection
		- -
	- Creating a virtual environment with Python 3.x and PEP 405
		- -
			- What does PUT do with a toy? #flashcard
				- Update an existing toy
		- -
		- -
			- Command to create a virtual environment in Linux: #flashcard
				- python3 -m venv ~/HillarDjangoREST/01
		- -
		- -
			- What does PUT do with a toy? #flashcard
				- Delete an existing toy
		- -
		- -
			- Command to make a virtual environment in PowerShell: #flashcard
				- python -m venv $env:userprofile\HillarDjangoREST\01
		- -
		- -
			- About urls in DRF. #flashcard
				- In a RESTful Web Service, each resource has its own unique URL. In our web service, each toy will have its own unique URL.
		- -
	- Activating the virtual environment
		- -
			- Steps to activate a virtual environment in PowerShell #flashcard
				- cd $env:USERPROFILE
				    HillarDjangoREST\01\Scripts\Activate.ps1
		- -
		- -
			- How do you start a virtual environment of Python in Linux? #flashcard
				- source ~/HillarDjangoREST/01/bin/activate
		- -
	- Test your knowledge
	- Deactivating the virtual environment
		- -
			- Which of the following commands creates a new app named books in Django? #flashcard
				- django startapp books
				  python django.py startapp books
				  python manage.py startapp books
		- -
		- -
			- How do you stop a virtual environment of Python in Linux? #flashcard
				- In macOS or Linux, just type deactivate and press Enter.
		- -
		- -
			- In Django, a subclass of which of the following classes represents a Django application and its configuration? #flashcard
				- django.apps.AppConfig
				  django.application.configuration
				  django.config.App
		- -
		- -
			- How do you stop a virtual environment of Python in Windows? #flashcard
				- In Windows PowerShell, you have to run the Deactivate.ps1 script in the Scripts folder.
		- -
	- Understanding Django folders, files, and configurations
		- -
			- What does GET do with a toy? #flashcard
				- Retrieve a single toy
		- -
		- -
			- About names #flashcard
				- Now, we have to add toys.apps.ToysConfig as one of the installed apps in the restful01/settings.py file that configures settings for the restful01 Django project. I built the previous string by concatenating many values as follows: app name + .apps. + class name, which is, toys + .apps. + ToysConfig. In addition, we have to add the rest_framework app to make it possible for us to use Django REST framework.
		- -
		- -
			- URLs of lists VS details #flashcard
				- When we refer to a collection, we will use a slash (/) as the last character for the URL, as in http://localhost:8000/toys/. When we refer to a single resource of the collection we won't use a slash (/) as the last character for the URL, as in http://localhost:8000/toys/5
		- -
	- Creating Django views combined with serializer classes
		- -
			- About Response #flashcard
				- The JSONResponse class is a subclass of the django.http.HttpResponse class. The django.http.HttpResponse superclass represents an HTTP response with string content.
		- -
	- Launching Django's development server
		- -
			- Why 0 instead of localhost in DRF? #flashcard
				- If we specify 0.0.0.0 as the desired IP address for IPv4 configurations, the development server will listen on every interface on port 8000
		- -
	- Understanding accepted and returned content types
		- -
			- Which is the Response format type in DRF? #flashcard
				- No matter the value indicated for the Accept request header key, the response is always in the JSON format.
		- -