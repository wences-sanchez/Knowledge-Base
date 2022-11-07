title:: How Do You Test That a Python Function Throws an Exception? (highlights)
deck:: [[Across-the-Net]]
author:: [[stackoverflow.com]]
full-title:: "How Do You Test That a Python Function Throws an Exception?"
category:: #articles
url:: https://stackoverflow.com/questions/129507/how-do-you-test-that-a-python-function-throws-an-exception

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- How can you assert an exception in python? #python #code #flashcard
		  id:: 64f11fa8-4bd1-4304-a133-7f4acf58cb37
			- import mymod
			  
			  class MyTestCase(unittest.TestCase):
			    def test1(self):
			        self.assertRaises(SomeCoolException, mymod.myfunc)
	- -