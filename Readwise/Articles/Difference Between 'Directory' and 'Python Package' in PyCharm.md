# Difference Between 'Directory' and 'Python Package' in PyCharm

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "Difference Between 'Directory' and 'Python Package' in PyCharm"\
category:: #articles\
url:: https://stackoverflow.com/questions/57317624/difference-between-directory-and-python-package-in-pycharm\

![](https://readwise-assets.s3.amazonaws.com/static/images/article1.be68295a7e40.png)
## Highlights
- id:: 63c669cd-2e9f-423a-9d80-18fbf878c258
  
  When to use Directory over Python Package?
     You can use "Python Package" when you want to put some modules in there which should be importable. PyCharm will automatically create an __init__.py for the directory. #flashcard
-
- id:: 63c669cd-4fce-4443-b4b0-51531c44a420
  
  Why not create everything as a Python Package?
     Not every subdirectory in a project should necessarily be a package. For example docs and tests are commonly just directories. #flashcard
-
- id:: 63c669cd-8267-4ed8-953f-ca326b9c09b7
  
  Does PyCharm mark a location as one or the other based on its name?
     PyCharm seems to mark the icon with a dot if the subdirectory name is a valid identifier and not a keyword, regardless of whether the subdirectory is a package or not. This is possibly because, in Python 3.3+, subdirs are also implicit namespace packages (they are still importable even when there is no __init__.py file).
     If you have a project associated with a Python 2.7 interpreter, you don't get the dot on the icon unless the __init__.py file is added, since implicit namespace packages are not a thing in Python 2. #flashcard
-