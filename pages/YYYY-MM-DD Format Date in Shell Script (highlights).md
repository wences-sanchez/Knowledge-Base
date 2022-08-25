title:: YYYY-MM-DD Format Date in Shell Script (highlights)
author:: [[stackoverflow.com]]
full-title:: "YYYY-MM-DD Format Date in Shell Script"
category:: #articles
url:: https://stackoverflow.com/questions/1401482/yyyy-mm-dd-format-date-in-shell-script

- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- How could you print the date in Bash? .code .bash #card
		- In bash (>=4.2) it is preferable to use printf's built-in date formatter (part of bash) rather than the external date (usually GNU date).
		  
		  As such:
	- -