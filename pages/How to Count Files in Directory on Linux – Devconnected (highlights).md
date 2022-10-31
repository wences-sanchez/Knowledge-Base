title:: How to Count Files in Directory on Linux – Devconnected (highlights)
deck:: [[Across-the-Net]]
author:: [[devconnected.com]]
full-title:: "How to Count Files in Directory on Linux – Devconnected"
category:: #articles
url:: https://devconnected.com/how-to-count-files-in-directory-on-linux/

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- How would you count the numbers of files inside a directory in the Linux Terminal? #flashcard
		  id:: bdd871e8-8940-480f-94b5-ef834206a9d3
			- In order to count files recursively on Linux, you have to use the “find” command and pipe it with the “wc” command in order to count the number of files.
			  $ find <directory> -type f | wc -l
			  As a reminder, the “find” command is used in order to search for files on your system. 
			  When used with the “-f” option, you are targeting ony files. 
			  By default, the “find” command does not stop at the first depth of the directory : it will explore every single subdirectory, making the file searching recursive.
			  For example, if you want to recursively count files in the “/etc” directory, you would write the following query :
			  $ find /etc -type f | wc -l
			  
			  2074
		- tags:: [[linux]]
	- -