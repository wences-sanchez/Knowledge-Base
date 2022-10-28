# Run a Function Only Once in a Class - Python

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "Run a Function Only Once in a Class - Python"\
category:: #articles\
url:: https://stackoverflow.com/questions/53830926/run-a-function-only-once-in-a-class-python\

![](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)

## Highlights
- 
 How to set a field only once in Python? #flashcard  #code #python 
    class MyClass(object):
     postgres_data = None
     def __init__(self):
     if not MyClass.postgres_data:
     MyClass.postgres_data = self.fetch_data()
     def fetch_data(self):
     pass

    
-
