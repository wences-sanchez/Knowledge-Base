title:: Unix / Linux: Grep Word Count Command (highlights)
deck:: [[Across-the-Net]]
author:: [[cyberciti.biz]]
full-title:: "Unix / Linux: Grep Word Count Command"
category:: #articles
url:: https://www.cyberciti.biz/faq/unix-linux-grep-word-count-command/

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- How could you count the number of one word in a file or files in Bash? #flashcard
		  id:: aee9207a-835f-463b-9690-b592f591545e
			- grep -c "word" file
			  grep -c "string" file
			  In this example, search for a word called ‘var’ and display a count of matching lines:
			  grep -c 'var' /etc/passwd
			  Sample outputs:
			  23
		- tags:: [[bash]]
	- -
	- -
		- grep -o -w 'foo' bar.txt | wc -w #flashcard
		  id:: 58f0f191-546d-4f51-892c-d4a2849b01b3
	- -