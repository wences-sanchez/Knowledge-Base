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
			- What is REST? #flashcard
			  id:: 3a1e033c-108f-42cc-9b42-aabfdd76a7ab
				- REST (short for Representational State Transfer) is the architectural style that has been driving modern and scalable web development recently.
		- -
		- -
			- What does POST do with a toy? #flashcard
			  id:: 96e548b6-2d8a-4ce3-9387-ec0705e1afd6
				- Create a new toy in the collection
		- -
	- Creating a virtual environment with Python 3.x and PEP 405
		- -
			- What does PUT do with a toy? #flashcard
			  id:: 242b6fcf-6887-4924-ae88-f2230d7aad8a
				- Update an existing toy
		- -
		- -
			- Command to create a virtual environment in Linux: #flashcard
			  id:: 0f296d97-dad4-497d-a01e-564d06884e4b
				- python3 -m venv ~/HillarDjangoREST/01
		- -
		- -
			- What does PUT do with a toy? #flashcard
			  id:: c478ac2f-4029-4972-a518-fa1942967b94
				- Delete an existing toy
		- -
		- -
			- Command to make a virtual environment in PowerShell: #flashcard
			  id:: 3559d484-22b8-403b-a466-42bf6af80520
				- python -m venv $env:userprofile\HillarDjangoREST\01
		- -
		- -
			- About urls in DRF. #flashcard
			  id:: 0475043a-3fd6-451e-894a-648caf326828
				- In a RESTful Web Service, each resource has its own unique URL. In our web service, each toy will have its own unique URL.
		- -
	- Activating the virtual environment
		- -
			- Steps to activate a virtual environment in PowerShell #flashcard
			  id:: 06b4195d-088e-4cdb-9cdc-a1f377e984d4
				- cd $env:USERPROFILE
				    HillarDjangoREST\01\Scripts\Activate.ps1
		- -
		- -
			- How do you start a virtual environment of Python in Linux? #flashcard
			  id:: a9a26213-bcbc-4062-aba3-6eaabc891482
				- source ~/HillarDjangoREST/01/bin/activate
		- -
	- Test your knowledge
	- Deactivating the virtual environment
		- -
			- Which of the following commands creates a new app named books in Django? #flashcard
			  id:: a2dceae4-6825-4e58-8a98-b9c3a4af3ced
				- django startapp books
				  python django.py startapp books
				  python manage.py startapp books
		- -
		- -
			- How do you stop a virtual environment of Python in Linux? #flashcard
			  id:: ebac71f2-6780-4993-aa3a-bafd2a7482f6
				- In macOS or Linux, just type deactivate and press Enter.
		- -
		- -
			- In Django, a subclass of which of the following classes represents a Django application and its configuration? #flashcard
			  id:: 760d27c8-3ccd-429f-8caa-9aa8feeb8de2
				- django.apps.AppConfig
				  django.application.configuration
				  django.config.App
		- -
		- -
			- How do you stop a virtual environment of Python in Windows? #flashcard
			  id:: 454e2e93-50ad-4e3e-881a-cc13f626edbe
				- In Windows PowerShell, you have to run the Deactivate.ps1 script in the Scripts folder.
		- -
	- Understanding Django folders, files, and configurations
		- -
			- What does GET do with a toy? #flashcard
			  id:: a16b2675-3262-42b4-a057-0ddf95cf891e
				- Retrieve a single toy
		- -
		- -
			- About names #flashcard
			  id:: c1f284c0-1f13-45c2-9bb2-fe18fcb9346a
				- Now, we have to add toys.apps.ToysConfig as one of the installed apps in the restful01/settings.py file that configures settings for the restful01 Django project. I built the previous string by concatenating many values as follows: app name + .apps. + class name, which is, toys + .apps. + ToysConfig. In addition, we have to add the rest_framework app to make it possible for us to use Django REST framework.
		- -
		- -
			- URLs of lists VS details #flashcard
			  id:: f3a32361-3bac-4bd4-b34e-ae8e0e37fe3a
				- When we refer to a collection, we will use a slash (/) as the last character for the URL, as in http://localhost:8000/toys/. When we refer to a single resource of the collection we won't use a slash (/) as the last character for the URL, as in http://localhost:8000/toys/5
		- -
	- Creating Django views combined with serializer classes
		- -
			- About Response #flashcard
			  id:: 79ead212-e79c-4526-9b7e-13d7fa222ec9
				- The JSONResponse class is a subclass of the django.http.HttpResponse class. The django.http.HttpResponse superclass represents an HTTP response with string content.
		- -
	- Launching Django's development server
		- -
			- Why 0 instead of localhost in DRF? #flashcard
			  id:: a9e91379-0ab8-497a-b10b-ad071ae55292
				- If we specify 0.0.0.0 as the desired IP address for IPv4 configurations, the development server will listen on every interface on port 8000
		- -
	- Understanding accepted and returned content types
		- -
			- Which is the Response format type in DRF? #flashcard
			  id:: 6d44fa1b-d30a-4088-bc26-2e9e9da7791c
				- No matter the value indicated for the Accept request header key, the response is always in the JSON format.
		- -