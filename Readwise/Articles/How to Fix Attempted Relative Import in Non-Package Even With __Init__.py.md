# How to Fix "Attempted Relative Import in Non-Package" Even With __Init__.py

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "How to Fix "Attempted Relative Import in Non-Package" Even With __Init__.py"\
category:: #articles\
url:: https://stackoverflow.com/questions/11536764/how-to-fix-attempted-relative-import-in-non-package-even-with-init-py\

![](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)
## Highlights
- id:: 63c669cf-baaa-4b70-a933-c8d3ddee0cd2
   About relative imports in Python modules and packages .python #flashcard 
    It depends on how you want to launch your script.
     If you want to launch your UnitTest from the command line in a classic way, that is:
     python tests/core_test.py
     Then, since in this case 'components' and 'tests' are siblings folders, you can import the relative module either using the insert or the append method of the sys.path module.
     Something like:
     import sys
     from os import path
     sys.path.append( path.dirname( path.dirname( path.abspath(__file__) ) ) )
     from components.core import GameLoopEvents
     Otherwise, you can launch your script with the '-m' argument (note that in this case, we are talking about a package, and thus you must not give the '.py' extension), that is:
     python -m pkg.tests.core_test
     In such a case, you can simply use the relative import as you were doing:
     from ..components.core import GameLoopEvents
     You can finally mix the two approaches, so that your script will work no matter how it is called.
     For example:
     if __name__ == '__main__':
     if __package__ is None:
     import sys
     from os import path
     sys.path.append( path.dirname( path.dirname( path.abspath(__file__) ) ) )
     from components.core import GameLoopEvents
     else:
     from ..components.core import GameLoopEvents
-