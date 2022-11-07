title:: BASH Shell Redirect Output and Errors to /Dev/Null (highlights)
deck:: [[Across-the-Net]]
author:: [[cyberciti.biz]]
full-title:: "BASH Shell Redirect Output and Errors to /Dev/Null"
category:: #articles
url:: https://www.cyberciti.biz/faq/how-to-redirect-output-and-errors-to-devnull/

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- What is the best way of using /dev/null redirection in Bash? .bash #flashcard
		  id:: 7001f637-de23-41e8-8a18-88f5f97e315f
			- Syntax to redirect error and output messages to /dev/null
			  The syntax discussed below works with Bourne-like shells, such as sh, ksh, and bash:
			  
			  
			  $ command > /dev/null 2>&1
			  $ ./script.sh > /dev/null 2>&1
			  $ ./example.pl > /dev/null 2>&1
			  
			  
			  OR
			  
			  
			  command &>/dev/null
			  job arg1 arg2 &>/dev/null
			  /path/to/script arg1 &>/dev/null
			  
			  
			  You can also use the same syntax for all your cronjobs to avoid emails and output / error messages:
			  @hourly /scripts/backup/nas.backup >/dev/null 2>&1
			  OR
			  @hourly /scripts/backup/nas.backup &>/dev/null
	- -