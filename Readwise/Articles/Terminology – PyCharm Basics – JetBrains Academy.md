# Terminology – PyCharm Basics – JetBrains Academy

deck:: [[Across-the-Net]]\
author:: [[hyperskill.org]]\
full-title:: "Terminology – PyCharm Basics – JetBrains Academy"\
category:: #articles\
url:: https://hyperskill.org/learn/step/6315\

![](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)
## Highlights
- id:: 63c669d5-89d1-4ae3-ad09-5b0d8d3d0822
   How to use if else in list comprehension .python #flashcard 
    Finally, we can introduce the else statement in list comprehension. The syntax here differs a bit: [x if condition else y for x in some_iterable]. Using this, we can, for example, get 0 in a new list for each negative number in the old list:
     old_list = [8, 13, -7, 4, -9, 2, 10]new_list = [num if num >= 0 else 0 for num in old_list]print(new_list)  # [8, 13, 0, 4, 0, 2, 10]
-