title:: Run a Function Only Once in a Class - Python (highlights) (1)
author:: [[stackoverflow.com]]
full-title:: "Run a Function Only Once in a Class - Python"
category:: #articles
url:: https://stackoverflow.com/questions/53830926/run-a-function-only-once-in-a-class-python

- Highlights first synced by [[Readwise]] [[Friday, 07-10-2022]]
	- -
	- How to set a field only once in Python? #flashcard
		- class MyClass(object):
		    postgres_data = None
		  
		    def __init__(self):
		        if not MyClass.postgres_data:
		            MyClass.postgres_data = self.fetch_data()
		  
		    def fetch_data(self):
		        pass
		- #code #python
	- -