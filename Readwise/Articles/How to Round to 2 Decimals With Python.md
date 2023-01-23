# How to Round to 2 Decimals With Python?

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "How to Round to 2 Decimals With Python?"\
category:: #articles\
url:: https://stackoverflow.com/questions/20457038/how-to-round-to-2-decimals-with-python\

![](https://readwise-assets.s3.amazonaws.com/static/images/article3.5c705a01b476.png)
## Highlights
- id:: 63c669d0-587d-4752-b59a-f768fe5ae5d2
   How can you set two decimals precision in Python? #flashcard 
    You can use the round function, which takes as its first argument the number and the second argument is the precision after the decimal point.
     In your case, it would be:
     answer = str(round(answer, 2))
-