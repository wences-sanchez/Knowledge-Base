# Bash Scripting Tutorial for Beginners - LinuxConfig.org

deck:: [[Across-the-Net]]\
author:: [[Lubos Rendek]]\
full-title:: "Bash Scripting Tutorial for Beginners - LinuxConfig.org"\
category:: #articles\
url:: https://linuxconfig.org/bash-scripting-tutorial-for-beginners\

![](https://readwise-assets.s3.amazonaws.com/static/images/article1.be68295a7e40.png)
## Highlights
- id:: 63c669ca-073a-4d5d-a7b8-24da9d5b7290
   What should be at the top of every script? #flashcard 
    all our scripts will include shell interpreter definition #!/bin/bash
-
- id:: 63c669ca-882c-467b-a4d3-be48366c4c98
   How can we make our file executable? #flashcard 
    chmod +x FILENAME
-
- id:: 63c669ca-834e-4feb-9290-94bc68ed9d7c
  
  By default, any newly created files are not executable regardless of its file extension suffix. #flashcard
-
- id:: 63c669ca-8853-40dc-9bfc-d01ce00b0db8
  
  In fact, the file extension on GNU/Linux systems mostly does not have any meaning apart from the fact, that upon the execution of ls command to list all files and directories it is immediately clear that file with extension .sh is plausibly a shell script and file with .jpg is likely to be a lossy compressed image. #flashcard
-
- id:: 63c669ca-37d5-46ff-9d91-0f25477ead38
   How can you get the current user inside a script? #flashcard 
    user=$(whoami)
-
- id:: 63c669ca-7cf2-429a-b76e-1edc7ea42a7a
   Different command outputs. #flashcard 
    The difference between stdout and stderr output is an essential concept as it allows us to a threat, that is, to redirect each output separately. The > notation is used to redirect stdout to a file whereas 2> notation is used to redirect stderr and &> is used to redirect both stdout and stderr.
-
- id:: 63c669ca-8ffb-4655-a77f-99b83a00d547
   Syntax of function. #flashcard 
    function total_files {
     find $1 -type f | wc -l
     }
-
- id:: 63c669ca-ec67-4657-8f45-1080713120b8
   if syntax #flashcard 
    if [ $num_a -lt $num_b ]; then
     echo "$num_a is less than $num_b!"
     fi
-
- id:: 63c669ca-3955-4725-b3a7-0f3325e04876
   How can you count the number of arguments passed? #flashcard 
    Using $# on Line 4, we are printing the total number of supplied arguments
-
- id:: 63c669ca-dbf9-4016-9dfe-989263ba9d4a
   for syntax #flashcard 
    for i in 1 2 3; do
     echo $i
     done
-
- id:: 63c669ca-8d25-4230-8b9d-372852aed656
   while syntax #flashcard 
    counter=0
     while [ $counter -lt 3 ]; do
     let counter+=1
     echo $counter
     done
-
- id:: 63c669ca-c20c-4122-839e-d22530a54068
   until syntax #flashcard 
    counter=6
     until [ $counter -lt 3 ]; do
     let counter-=1
     echo $counter
     done
-