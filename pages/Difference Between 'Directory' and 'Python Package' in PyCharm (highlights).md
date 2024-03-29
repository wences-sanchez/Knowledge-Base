title:: Difference Between 'Directory' and 'Python Package' in PyCharm (highlights)
deck:: [[Across-the-Net]]
author:: [[stackoverflow.com]]
full-title:: "Difference Between 'Directory' and 'Python Package' in PyCharm"
category:: #articles
url:: https://stackoverflow.com/questions/57317624/difference-between-directory-and-python-package-in-pycharm

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- When to use Directory over Python Package?
		  id:: f0dfbbfa-5e60-4077-af1a-5d549b087c32
		  
		  
		  You can use "Python Package" when you want to put some modules in there which should be importable. PyCharm will automatically create an __init__.py for the directory. #flashcard
	- -
	- -
		- Why not create everything as a Python Package?
		  id:: 1c6351fa-75e0-4a25-a3f9-794958c4b77b
		  
		  
		  Not every subdirectory in a project should necessarily be a package.  For example docs and tests are commonly just directories. #flashcard
	- -
	- -
		- Does PyCharm mark a location as one or the other based on its name?
		  id:: 02768f93-d99e-40bc-9c7f-e3c6a4c609e7
		  
		  
		  PyCharm seems to mark the icon with a dot if the subdirectory name is a valid identifier and not a keyword, regardless of whether the subdirectory is a package or not. This is possibly because, in Python 3.3+, subdirs are also implicit namespace packages (they are still importable even when there is no __init__.py file).
		  
		  If you have a project associated with a Python 2.7 interpreter, you don't get the dot on the icon unless the __init__.py file is added, since implicit namespace packages are not a thing in Python 2. #flashcard
	- -