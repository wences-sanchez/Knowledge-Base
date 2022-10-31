title:: Django RESTful Web Services (highlights)
deck:: [[O'Reilly-Learning::Django RESTful Web Services]]
author:: [[]]
full-title:: "Django RESTful Web Services"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Preface
	- Defining the requirements for our first RESTful Web Service
		- -
		- REST (short for Representational State Transfer) is the architectural style that has been driving modern and scalable web development recently. #flashcard
			- What is REST?
		- -
		- -
		- Create a new toy in the collection #flashcard
			- What does POST do with a toy?
		- -
	- Creating a virtual environment with Python 3.x and PEP 405
		- -
		- Update an existing toy #flashcard
			- What does PUT do with a toy?
		- -
		- -
		- python3 -m venv ~/HillarDjangoREST/01 #flashcard
			- Command to create a virtual environment in Linux:
		- -
		- -
		- Delete an existing toy #flashcard
			- What does PUT do with a toy?
		- -
		- -
		- python -m venv $env:userprofile\HillarDjangoREST\01 #flashcard
			- Command to make a virtual environment in PowerShell:
		- -
		- -
		- In a RESTful Web Service, each resource has its own unique URL. In our web service, each toy will have its own unique URL. #flashcard
			- About urls in DRF.
		- -
	- Activating the virtual environment
		- -
		- cd $env:USERPROFILE
		    HillarDjangoREST\01\Scripts\Activate.ps1 #flashcard
			- Steps to activate a virtual environment in PowerShell
		- -
		- -
		- source ~/HillarDjangoREST/01/bin/activate #flashcard
			- How do you start a virtual environment of Python in Linux?
		- -
	- Test your knowledge
	- Deactivating the virtual environment
		- -
		- django startapp books
		  python django.py startapp books
		  python manage.py startapp books #flashcard
			- Which of the following commands creates a new app named books in Django?
		- -
		- -
		- In macOS or Linux, just type deactivate and press Enter. #flashcard
			- How do you stop a virtual environment of Python in Linux?
		- -
		- -
		- django.apps.AppConfig
		  django.application.configuration
		  django.config.App #flashcard
			- In Django, a subclass of which of the following classes represents a Django application and its configuration?
		- -
		- -
		- In Windows PowerShell, you have to run the Deactivate.ps1 script in the Scripts folder. #flashcard
			- How do you stop a virtual environment of Python in Windows?
		- -
	- Understanding Django folders, files, and configurations
		- -
		- Retrieve a single toy #flashcard
			- What does GET do with a toy?
		- -
		- -
		- Now, we have to add toys.apps.ToysConfig as one of the installed apps in the restful01/settings.py file that configures settings for the restful01 Django project. I built the previous string by concatenating many values as follows: app name + .apps. + class name, which is, toys + .apps. + ToysConfig. In addition, we have to add the rest_framework app to make it possible for us to use Django REST framework. #flashcard
			- About names
		- -
		- -
		- When we refer to a collection, we will use a slash (/) as the last character for the URL, as in http://localhost:8000/toys/. When we refer to a single resource of the collection we won't use a slash (/) as the last character for the URL, as in http://localhost:8000/toys/5 #flashcard
			- URLs of lists VS details
		- -
	- Creating Django views combined with serializer classes
		- -
		- The JSONResponse class is a subclass of the django.http.HttpResponse class. The django.http.HttpResponse superclass represents an HTTP response with string content. #flashcard
			- About Response
		- -
	- Launching Django's development server
		- -
		- If we specify 0.0.0.0 as the desired IP address for IPv4 configurations, the development server will listen on every interface on port 8000 #flashcard
			- Why 0 instead of localhost in DRF?
		- -
	- Understanding accepted and returned content types
		- -
		- No matter the value indicated for the Accept request header key, the response is always in the JSON format. #flashcard
			- Which is the Response format type in DRF?
		- -