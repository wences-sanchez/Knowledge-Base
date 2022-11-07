# Difference Between 'Directory' and 'Python Package' in PyCharm

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "Difference Between 'Directory' and 'Python Package' in PyCharm"\
category:: #articles\
url:: https://stackoverflow.com/questions/57317624/difference-between-directory-and-python-package-in-pycharm\

![](https://readwise-assets.s3.amazonaws.com/static/images/article1.be68295a7e40.png)
## Highlights
- id:: 63639906-902e-422c-83fa-983e95b206a3
  
  When to use Directory over Python Package?
     You can use "Python Package" when you want to put some modules in there which should be importable. PyCharm will automatically create an __init__.py for the directory. #flashcard
-
- id:: 63639906-be69-480d-96d2-2686a5680f85
  
  Why not create everything as a Python Package?
     Not every subdirectory in a project should necessarily be a package. For example docs and tests are commonly just directories. #flashcard
-
- id:: 63639906-06c5-447d-9374-9edfd4edbdb4
  
  Does PyCharm mark a location as one or the other based on its name?
     PyCharm seems to mark the icon with a dot if the subdirectory name is a valid identifier and not a keyword, regardless of whether the subdirectory is a package or not. This is possibly because, in Python 3.3+, subdirs are also implicit namespace packages (they are still importable even when there is no __init__.py file).
     If you have a project associated with a Python 2.7 interpreter, you don't get the dot on the icon unless the __init__.py file is added, since implicit namespace packages are not a thing in Python 2. #flashcard
-