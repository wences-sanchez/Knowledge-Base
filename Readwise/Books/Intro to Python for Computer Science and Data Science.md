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
- id:: 63c66a08-8ced-49a6-b72e-aaa821b5cc80
   Method to make the character low #flashcard 
    s.lower()
-
- id:: 63c66a08-2d1c-4e97-8f93-257d54686204
   Method to set all the characters small #flashcard 
    s.upper()
-
### 10.4 Properties for Data Access
- id:: 63c66a08-a96c-4107-b60c-e51fcb696035
   Example of @property #flashcard 
    @property
     14 def hour(self):
     15 """Return the hour."""
     16 return self._hour
-
- id:: 63c66a08-46c9-47b5-98aa-d79cdd161f55
   Example of setter #flashcard 
    @hour.setter
     19 def hour(self, hour):
     20 """Set the hour."""
     21 if not (0 <= hour < 24):
     22 raise ValueError(f'Hour ({hour}) must be 0-23')
     23
     24 self._hour = hour
-