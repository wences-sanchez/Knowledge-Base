# How to Count Files in Directory on Linux – Devconnected

deck:: [[Across-the-Net]]\
author:: [[devconnected.com]]\
full-title:: "How to Count Files in Directory on Linux – Devconnected"\
category:: #articles\
url:: https://devconnected.com/how-to-count-files-in-directory-on-linux/\

![](https://readwise-assets.s3.amazonaws.com/static/images/article1.be68295a7e40.png)
## Highlights
- id:: 63639907-088f-43bc-9de3-b88bd28a5398
   How would you count the numbers of files inside a directory in the Linux Terminal? #flashcard  #linux 
    In order to count files recursively on Linux, you have to use the “find” command and pipe it with the “wc” command in order to count the number of files.
     $ find <directory> -type f | wc -l
     As a reminder, the “find” command is used in order to search for files on your system. 
     When used with the “-f” option, you are targeting ony files. 
     By default, the “find” command does not stop at the first depth of the directory : it will explore every single subdirectory, making the file searching recursive.
     For example, if you want to recursively count files in the “/etc” directory, you would write the following query :
     $ find /etc -type f | wc -l
     2074
-