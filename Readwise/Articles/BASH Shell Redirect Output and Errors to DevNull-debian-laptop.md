# BASH Shell Redirect Output and Errors to /Dev/Null

deck:: [[Across-the-Net]]\
author:: [[cyberciti.biz]]\
full-title:: "BASH Shell Redirect Output and Errors to /Dev/Null"\
category:: #articles\
url:: https://www.cyberciti.biz/faq/how-to-redirect-output-and-errors-to-devnull/\

![](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)
## Highlights
- id:: 63639904-5913-4fec-84b7-fce40351265d
   What is the best way of using /dev/null redirection in Bash? .bash #flashcard 
    Syntax to redirect error and output messages to /dev/null
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
-