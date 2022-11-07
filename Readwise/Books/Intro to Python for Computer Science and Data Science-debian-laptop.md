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
- id:: 6363991d-3e13-4198-afac-2793e4028f03
   Method to make the character low #flashcard 
    s.lower()
-
- id:: 6363991d-9a45-43db-ae45-d2af376d318b
   Method to set all the characters small #flashcard 
    s.upper()
-
### 10.4 Properties for Data Access
- id:: 6363991d-e2ee-4630-86d4-86bcac4a4fce
   Example of @property #flashcard 
    @property
     14 def hour(self):
     15 """Return the hour."""
     16 return self._hour
-
- id:: 6363991d-73de-41ee-9d39-587bd557cc9e
   Example of setter #flashcard 
    @hour.setter
     19 def hour(self, hour):
     20 """Set the hour."""
     21 if not (0 <= hour < 24):
     22 raise ValueError(f'Hour ({hour}) must be 0-23')
     23
     24 self._hour = hour
-