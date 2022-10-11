title:: How Do You Test That a Python Function Throws an Exception? (highlights)
author:: [[stackoverflow.com]]
full-title:: "How Do You Test That a Python Function Throws an Exception?"
category:: #articles
url:: https://stackoverflow.com/questions/129507/how-do-you-test-that-a-python-function-throws-an-exception

- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- How can you assert an exception in python? #python #code #car
	  id:: 63401517-2689-4fc7-a78d-d21ff758524e
		- import mymod
		  
		  class MyTestCase(unittest.TestCase):
		    def test1(self):
		        self.assertRaises(SomeCoolException, mymod.myfunc)
	- -