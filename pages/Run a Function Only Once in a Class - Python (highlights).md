title:: Run a Function Only Once in a Class - Python (highlights)
deck:: [[Across-the-Net]]
author:: [[stackoverflow.com]]
full-title:: "Run a Function Only Once in a Class - Python"
category:: #articles
url:: https://stackoverflow.com/questions/53830926/run-a-function-only-once-in-a-class-python

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- How to set a field only once in Python? #flashcard
			- class MyClass(object):
			    postgres_data = None
			  
			    def __init__(self):
			        if not MyClass.postgres_data:
			            MyClass.postgres_data = self.fetch_data()
			  
			    def fetch_data(self):
			        pass
		- tags:: [[code]] [[python]]
	- -