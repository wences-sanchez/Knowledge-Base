title:: YYYY-MM-DD Format Date in Shell Script (highlights)
deck:: [[Across-the-Net]]
author:: [[stackoverflow.com]]
full-title:: "YYYY-MM-DD Format Date in Shell Script"
category:: #articles
url:: https://stackoverflow.com/questions/1401482/yyyy-mm-dd-format-date-in-shell-script

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- How could you print the date in Bash? .code .bash #flashcard
		  id:: 86f08a21-705f-4739-8646-cef5e7a3f796
			- In bash (>=4.2) it is preferable to use printf's built-in date formatter (part of bash) rather than the external date (usually GNU date).
			  
			  As such:
	- -