title:: Intro to Python for Computer Science and Data Science (highlights)
author:: [[]]
full-title:: "Intro to Python for Computer Science and Data Science"
category:: #books

tags:: #[[O'Reilly-Learning]]

- #tags #[[O'Reilly-Learning]]
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- 4.12 Methods: Functions That Belong to Objects
		- -
		- Method to make the character low #car
			- s.lower()
		- -
		- -
		- Method to set all the characters small #car
			- s.upper()
		- -
	- 10.4 Properties for Data Access
		- -
		- Example of @property #car
			- @property
			  14 def hour(self):
			  15     """Return the hour."""
			  16     return self._hour
		- -
		- -
		- Example of setter #car
			- @hour.setter
			  19 def hour(self, hour):
			  20     """Set the hour."""
			  21     if not (0 <= hour < 24):
			  22         raise ValueError(f'Hour ({hour}) must be 0-23')
			  23
			  24     self._hour = hour
		- -