title:: How to Add a Directory to the PATH? (highlights)
author:: [[askubuntu.com]]
full-title:: "How to Add a Directory to the PATH?"
category:: #articles
url:: https://askubuntu.com/questions/60218/how-to-add-a-directory-to-the-path

- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- How can you add a folder to PATH in Linux? #card
		- Edit .bashrc in your home directory and add the following line:
		  
		  export PATH="/path/to/dir:$PATH"
		  
		  
		  You will need to source your .bashrc or logout/login (or restart the terminal) for the changes to take effect. To source your .bashrc, simply type
		  
		  $ source ~/.bashrc
	- -