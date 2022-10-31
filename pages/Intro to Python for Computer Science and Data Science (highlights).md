title:: Intro to Python for Computer Science and Data Science (highlights)
deck:: [[O'Reilly-Learning::Intro to Python for Computer Science and Data Science]]
author:: [[]]
full-title:: "Intro to Python for Computer Science and Data Science"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- 4.12 Methods: Functions That Belong to Objects
		- -
			- Method to make the character low #flashcard
			  id:: 2030ad62-bc6b-4163-ad34-597c86ef1714
				- s.lower()
		- -
		- -
			- Method to set all the characters small #flashcard
			  id:: 2e12710d-8661-4e14-ae2a-03ebb58c318d
				- s.upper()
		- -
	- 10.4 Properties for Data Access
		- -
			- Example of @property #flashcard
			  id:: fd7d57aa-74b9-44e2-aba0-830a63cca43a
				- @property
				  14 def hour(self):
				  15     """Return the hour."""
				  16     return self._hour
		- -
		- -
			- Example of setter #flashcard
			  id:: a0a09e01-c774-4260-b08a-a5ce55d49204
				- @hour.setter
				  19 def hour(self, hour):
				  20     """Set the hour."""
				  21     if not (0 <= hour < 24):
				  22         raise ValueError(f'Hour ({hour}) must be 0-23')
				  23
				  24     self._hour = hour
		- -