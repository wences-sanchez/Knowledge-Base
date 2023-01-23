# How Do I Do a Case-Insensitive String Comparison?

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "How Do I Do a Case-Insensitive String Comparison?"\
category:: #articles\
url:: https://stackoverflow.com/questions/319426/how-do-i-do-a-case-insensitive-string-comparison\

![](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)
## Highlights
- id:: 63c669ce-b688-42d9-b4d0-d686d3cfcaa6
   How can you compare two strings case insensitive in Python? .python .tips #flashcard 
    string1 = 'Hello'
     string2 = 'hello'
     if string1.lower() == string2.lower():
     print("The strings are the same (case insensitive)")
     else:
     print("The strings are NOT the same (case insensitive)")
-