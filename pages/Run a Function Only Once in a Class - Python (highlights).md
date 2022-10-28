title:: Run a Function Only Once in a Class - Python (highlights)
author:: [[stackoverflow.com]]
full-title:: "Run a Function Only Once in a Class - Python"
category:: #articles
url:: https://stackoverflow.com/questions/53830926/run-a-function-only-once-in-a-class-python

- Highlights first synced by [[Readwise]] [[Friday, 28-10-2022]]
	- class MyClass(object):
	    postgres_data = None
	  
	    def __init__(self):
	        if not MyClass.postgres_data:
	            MyClass.postgres_data = self.fetch_data()
	  
	    def fetch_data(self):
	        pass
		- **Tags**: #[[code]] #[[python]]
		- **Note**: How to set a field only once in Python?