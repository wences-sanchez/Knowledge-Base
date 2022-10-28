# Intro to Python for Computer Science and Data Science

deck:: [[O'Reilly-Learning::Intro to Python for Computer Science and Data Science]]\
author:: [[None]]\
full-title:: "Intro to Python for Computer Science and Data Science"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/intro-to-python/9780135404799/ibis_generated_cover_thumbnail.jpg)

## Highlights
### 4.12 Methods: Functions That Belong to Objects
- 
 Method to make the character low #flashcard 
    s.lower()

    
-
- 
 Method to set all the characters small #flashcard 
    s.upper()

    
-
### 10.4 Properties for Data Access
- 
 Example of @property #flashcard 
    @property
     14 def hour(self):
     15 """Return the hour."""
     16 return self._hour

    
-
- 
 Example of setter #flashcard 
    @hour.setter
     19 def hour(self, hour):
     20 """Set the hour."""
     21 if not (0 <= hour < 24):
     22 raise ValueError(f'Hour ({hour}) must be 0-23')
     23
     24 self._hour = hour

    
-
