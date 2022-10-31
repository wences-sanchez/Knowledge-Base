title:: Intro to Python for Computer Science and Data Science (highlights)
deck:: [[O'Reilly-Learning::Intro to Python for Computer Science and Data Science]]
author:: [[]]
full-title:: "Intro to Python for Computer Science and Data Science"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- 4.12 Methods: Functions That Belong to Objects
		- -
		- s.lower() #flashcard
			- Method to make the character low
		- -
		- -
		- s.upper() #flashcard
			- Method to set all the characters small
		- -
	- 10.4 Properties for Data Access
		- -
		- @property
		  14 def hour(self):
		  15     """Return the hour."""
		  16     return self._hour #flashcard
			- Example of @property
		- -
		- -
		- @hour.setter
		  19 def hour(self, hour):
		  20     """Set the hour."""
		  21     if not (0 <= hour < 24):
		  22         raise ValueError(f'Hour ({hour}) must be 0-23')
		  23
		  24     self._hour = hour #flashcard
			- Example of setter
		- -