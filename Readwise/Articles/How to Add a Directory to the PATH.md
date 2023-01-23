# How to Add a Directory to the PATH?

deck:: [[Across-the-Net]]\
author:: [[askubuntu.com]]\
full-title:: "How to Add a Directory to the PATH?"\
category:: #articles\
url:: https://askubuntu.com/questions/60218/how-to-add-a-directory-to-the-path\

![](https://readwise-assets.s3.amazonaws.com/static/images/article4.6bc1851654a0.png)
## Highlights
- id:: 63c669cf-bd3c-4478-8269-5750c28a02df
   How can you add a folder to PATH in Linux? #flashcard 
    Edit .bashrc in your home directory and add the following line:
     export PATH="/path/to/dir:$PATH"
     You will need to source your .bashrc or logout/login (or restart the terminal) for the changes to take effect. To source your .bashrc, simply type
     $ source ~/.bashrc
-