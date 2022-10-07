title:: Unix / Linux: Grep Word Count Command (highlights) (1)
author:: [[cyberciti.biz]]
full-title:: "Unix / Linux: Grep Word Count Command"
category:: #articles
url:: https://www.cyberciti.biz/faq/unix-linux-grep-word-count-command/

- Highlights first synced by [[Readwise]] [[Friday, 07-10-2022]]
	- -
	- How could you count the number of one word in a file or files in Bash? #flashcard
		- grep -c "word" file
		  grep -c "string" file
		  In this example, search for a word called ‘var’ and display a count of matching lines:
		  grep -c 'var' /etc/passwd
		  Sample outputs:
		  23
		- #bash
	- -
	- -
	- grep -o -w 'foo' bar.txt | wc -w #spaced
	- -