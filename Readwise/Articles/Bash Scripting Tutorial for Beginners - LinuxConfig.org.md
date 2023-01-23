# Bash Scripting Tutorial for Beginners - LinuxConfig.org

deck:: [[Across-the-Net]]\
author:: [[linuxconfig.org]]\
full-title:: "Bash Scripting Tutorial for Beginners - LinuxConfig.org"\
category:: #articles\
url:: https://linuxconfig.org/bash-scripting-tutorial-for-beginners\

![](https://readwise-assets.s3.amazonaws.com/static/images/article4.6bc1851654a0.png)
## Highlights
- id:: 63c669ca-2ef0-4b23-a3d7-c3ffc3d67dc1
   What should be at the top of every script? #flashcard 
    all our scripts will include shell interpreter definition #!/bin/bash
-
- id:: 63c669ca-2bf8-4131-962f-3d555f58eb65
   How can we make our file executable? #flashcard 
    chmod +x FILENAME
-
- id:: 63c669ca-bbd5-4a5b-915b-0ae99280be3e
  
  By default, any newly created files are not executable regardless of its file extension suffix. #flashcard
-
- id:: 63c669ca-6e31-4078-9d9f-d1791f3b27e7
  
  In fact, the file extension on GNU/Linux systems mostly does not have any meaning apart from the fact, that upon the execution of ls command to list all files and directories it is immediately clear that file with extension .sh is plausibly a shell script and file with .jpg is likely to be a lossy compressed image. #flashcard
-
- id:: 63c669ca-823c-419f-842d-d963d530b788
   How can you get the current user inside a script? #flashcard 
    user=$(whoami)
-
- id:: 63c669ca-576d-4f03-9e37-9c204b1866ba
   Different command outputs. #flashcard 
    The difference between stdout and stderr output is an essential concept as it allows us to a threat, that is, to redirect each output separately. The > notation is used to redirect stdout to a file whereas 2> notation is used to redirect stderr and &> is used to redirect both stdout and stderr.
-
- id:: 63c669ca-894a-4e7b-af08-2bff8b79429f
   Syntax of function. #flashcard 
    function total_files {
     find $1 -type f | wc -l
     }
-
- id:: 63c669ca-7ee9-42c6-a971-9bf176680737
   if syntax #flashcard 
    if [ $num_a -lt $num_b ]; then
     echo "$num_a is less than $num_b!"
     fi
-
- id:: 63c669ca-10a9-4e46-8eb7-fc25cc6ed1d0
   How can you count the number of arguments passed? #flashcard 
    Using $# on Line 4, we are printing the total number of supplied arguments
-
- id:: 63c669ca-0887-4198-ae1e-763317441ca3
   for syntax #flashcard 
    for i in 1 2 3; do
     echo $i
     done
-
- id:: 63c669ca-8ee7-429a-b6b1-d87569f5d706
   while syntax #flashcard 
    counter=0
     while [ $counter -lt 3 ]; do
     let counter+=1
     echo $counter
     done
-
- id:: 63c669ca-75ce-49ad-91d1-64ca6989f458
   until syntax #flashcard 
    counter=6
     until [ $counter -lt 3 ]; do
     let counter-=1
     echo $counter
     done
-