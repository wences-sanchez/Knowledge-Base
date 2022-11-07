# Bash Scripting Tutorial for Beginners - LinuxConfig.org

deck:: [[Across-the-Net]]\
author:: [[Lubos Rendek]]\
full-title:: "Bash Scripting Tutorial for Beginners - LinuxConfig.org"\
category:: #articles\
url:: https://linuxconfig.org/bash-scripting-tutorial-for-beginners\

![](https://readwise-assets.s3.amazonaws.com/static/images/article1.be68295a7e40.png)
## Highlights
- id:: 63639904-d438-49ed-888a-2146f954809d
   What should be at the top of every script? #flashcard 
    all our scripts will include shell interpreter definition #!/bin/bash
-
- id:: 63639904-2d70-470c-8cbd-3c931d8d4a67
   How can we make our file executable? #flashcard 
    chmod +x FILENAME
-
- id:: 63639904-d1f5-4d7d-86f5-cc4f8e2f3717
  
  By default, any newly created files are not executable regardless of its file extension suffix. #flashcard
-
- id:: 63639904-2750-4c53-8b21-9e10f7ab6680
  
  In fact, the file extension on GNU/Linux systems mostly does not have any meaning apart from the fact, that upon the execution of ls command to list all files and directories it is immediately clear that file with extension .sh is plausibly a shell script and file with .jpg is likely to be a lossy compressed image. #flashcard
-
- id:: 63639904-bdff-4e70-a348-fac79ecf1109
   How can you get the current user inside a script? #flashcard 
    user=$(whoami)
-
- id:: 63639904-994a-4e53-bfe6-62efe3a9a08c
   Different command outputs. #flashcard 
    The difference between stdout and stderr output is an essential concept as it allows us to a threat, that is, to redirect each output separately. The > notation is used to redirect stdout to a file whereas 2> notation is used to redirect stderr and &> is used to redirect both stdout and stderr.
-
- id:: 63639904-a368-49e6-abf9-26ef4bc2b6cb
   Syntax of function. #flashcard 
    function total_files {
     find $1 -type f | wc -l
     }
-
- id:: 63639904-65c1-4f8f-a6fc-d6881b283a3b
   if syntax #flashcard 
    if [ $num_a -lt $num_b ]; then
     echo "$num_a is less than $num_b!"
     fi
-
- id:: 63639904-e1cf-45c6-9407-b35529173dfe
   How can you count the number of arguments passed? #flashcard 
    Using $# on Line 4, we are printing the total number of supplied arguments
-
- id:: 63639904-9c08-4c80-9c0c-f57e83ccc715
   for syntax #flashcard 
    for i in 1 2 3; do
     echo $i
     done
-
- id:: 63639904-4615-4bca-bdde-e34b6a5eaab1
   while syntax #flashcard 
    counter=0
     while [ $counter -lt 3 ]; do
     let counter+=1
     echo $counter
     done
-
- id:: 63639904-6c33-42f0-adb9-ac90ca242600
   until syntax #flashcard 
    counter=6
     until [ $counter -lt 3 ]; do
     let counter-=1
     echo $counter
     done
-