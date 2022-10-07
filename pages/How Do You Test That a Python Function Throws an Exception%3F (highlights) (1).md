title:: How Do You Test That a Python Function Throws an Exception? (highlights) (1)
author:: [[stackoverflow.com]]
full-title:: "How Do You Test That a Python Function Throws an Exception?"
category:: #articles
url:: https://stackoverflow.com/questions/129507/how-do-you-test-that-a-python-function-throws-an-exception

- Highlights first synced by [[Readwise]] [[Friday, 07-10-2022]]
	- -
	- How can you assert an exception in python? #python #code #flashcard
		- import mymod
		  
		  class MyTestCase(unittest.TestCase):
		    def test1(self):
		        self.assertRaises(SomeCoolException, mymod.myfunc)
	- -