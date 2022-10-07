title:: Python object.__repr__(self) should be an expression? (highlights) (1)
author:: [[Roger Pate]]
full-title:: "Python object.__repr__(self) should be an expression?"
category:: #articles
url:: https://stackoverflow.com/questions/452300/python-object-repr-self-should-be-an-expression

- Highlights first synced by [[Readwise]] [[Friday, 07-10-2022]]
	- -
	- >>> from datetime import date
	  >>>
	  >>> repr(date.today())        # calls date.today().__repr__()
	  'datetime.date(2009, 1, 16)'
	  >>> eval(_)                   # _ is the output of the last command
	  datetime.date(2009, 1, 16)
	  
	  The output is a string that can be parsed by the python interpreter and results in an equal object.
	  
	  If that's not possible, it should return a string in the form of <...some useful description...>. #spaced
	- -