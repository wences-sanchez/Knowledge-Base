# What's a Command Line Way to Find Large Files/Directories to Remove and Free Up Space?

deck:: [[Across-the-Net]]\
author:: [[askubuntu.com]]\
full-title:: "What's a Command Line Way to Find Large Files/Directories to Remove and Free Up Space?"\
category:: #articles\
url:: https://askubuntu.com/questions/36111/whats-a-command-line-way-to-find-large-files-directories-to-remove-and-free-up\

![](https://readwise-assets.s3.amazonaws.com/static/images/article0.00998d930354.png)

## Highlights
- 
 How can you find all files in your Linux distro which are bigger than 10MiB through the terminal? .code .linux #flashcard 
    If you just need to find large files, you can use find with the -size option. The next command will list all files larger than 10MiB (not to be confused with 10MB):
     find / -size +10M -ls

    
-
