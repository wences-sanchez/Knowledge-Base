title:: Python object.__repr__(self) should be an expression? (highlights)
deck:: [[Across-the-Net]]
author:: [[Roger Pate]]
full-title:: "Python object.__repr__(self) should be an expression?"
category:: #articles
url:: https://stackoverflow.com/questions/452300/python-object-repr-self-should-be-an-expression

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- id:: 27359538-d9ea-4838-96b7-7981a2b39788
		  >>> from datetime import date
		  >>>
		  >>> repr(date.today())        # calls date.today().__repr__()
		  'datetime.date(2009, 1, 16)'
		  >>> eval(_)                   # _ is the output of the last command
		  datetime.date(2009, 1, 16)
		  
		  The output is a string that can be parsed by the python interpreter and results in an equal object.
		  
		  If that's not possible, it should return a string in the form of <...some useful description...>. #flashcard
	- -