# How to Import the Class Within the Same Directory or Sub Directory?

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "How to Import the Class Within the Same Directory or Sub Directory?"\
category:: #articles\
url:: https://stackoverflow.com/questions/4142151/how-to-import-the-class-within-the-same-directory-or-sub-directory\

![](https://readwise-assets.s3.amazonaws.com/static/images/article1.be68295a7e40.png)
## Highlights
- id:: 63c669cf-ebfe-46de-b2b9-388db7e3b250
  
  Python 2
     Make an empty file called __init__.py in the same directory as the files. That will signify to Python that it's "ok to import from this directory".
     Then just do...
     from user import User
     from dir import Dir
     The same holds true if the files are in a subdirectory - put an __init__.py in the subdirectory as well, and then use regular import statements, with dot notation. For each level of directory, you need to add to the import path. 
     bin/
     main.py
     classes/
     user.py
     dir.py
     So if the directory was named "classes", then you'd do this:
     from classes.user import User
     from classes.dir import Dir
     Python 3
     Same as previous, but prefix the module name with a . if not using a subdirectory:
     from .user import User
     from .dir import Dir #flashcard
-