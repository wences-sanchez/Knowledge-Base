# How Do You Test That a Python Function Throws an Exception?

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "How Do You Test That a Python Function Throws an Exception?"\
category:: #articles\
url:: https://stackoverflow.com/questions/129507/how-do-you-test-that-a-python-function-throws-an-exception\

![](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)
## Highlights
- id:: 63c669cf-b2f1-4e21-9fab-f9af55628c63
   How can you assert an exception in python? #python #code #flashcard 
    import mymod
     class MyTestCase(unittest.TestCase):
     def test1(self):
     self.assertRaises(SomeCoolException, mymod.myfunc)
-