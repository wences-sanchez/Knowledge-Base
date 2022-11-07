# Unix / Linux: Grep Word Count Command

deck:: [[Across-the-Net]]\
author:: [[cyberciti.biz]]\
full-title:: "Unix / Linux: Grep Word Count Command"\
category:: #articles\
url:: https://www.cyberciti.biz/faq/unix-linux-grep-word-count-command/\

![](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)
## Highlights
- id:: 63639909-71c1-432b-9f41-83636fd17629
   How could you count the number of one word in a file or files in Bash? #flashcard  #bash 
    grep -c "word" file
     grep -c "string" file
     In this example, search for a word called ‘var’ and display a count of matching lines:
     grep -c 'var' /etc/passwd
     Sample outputs:
     23
-
- id:: 63639909-6876-4ef0-8c5a-adb22f05d44d
  
  grep -o -w 'foo' bar.txt | wc -w #flashcard
-