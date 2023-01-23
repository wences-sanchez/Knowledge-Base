# Unix / Linux: Grep Word Count Command

deck:: [[Across-the-Net]]\
author:: [[cyberciti.biz]]\
full-title:: "Unix / Linux: Grep Word Count Command"\
category:: #articles\
url:: https://www.cyberciti.biz/faq/unix-linux-grep-word-count-command/\

![](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)
## Highlights
- id:: 63c669d7-82c7-4c62-9da1-728ff3cf295b
   How could you count the number of one word in a file or files in Bash? #flashcard  #bash 
    grep -c "word" file
     grep -c "string" file
     In this example, search for a word called ‘var’ and display a count of matching lines:
     grep -c 'var' /etc/passwd
     Sample outputs:
     23
-
- id:: 63c669d7-f9c4-40a8-86d2-a331f9b8ca5e
  
  grep -o -w 'foo' bar.txt | wc -w #flashcard
-