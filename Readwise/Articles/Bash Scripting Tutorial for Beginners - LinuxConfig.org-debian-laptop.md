# Bash Scripting Tutorial for Beginners - LinuxConfig.org

deck:: [[Across-the-Net]]\
author:: [[linuxconfig.org]]\
full-title:: "Bash Scripting Tutorial for Beginners - LinuxConfig.org"\
category:: #articles\
url:: https://linuxconfig.org/bash-scripting-tutorial-for-beginners\

![](https://readwise-assets.s3.amazonaws.com/static/images/article4.6bc1851654a0.png)
## Highlights
- id:: 63639904-e745-4bfd-809c-9edfada9c6c1
   What should be at the top of every script? #flashcard 
    all our scripts will include shell interpreter definition #!/bin/bash
-
- id:: 63639904-b30c-4595-be17-c8e0188f0d47
   How can we make our file executable? #flashcard 
    chmod +x FILENAME
-
- id:: 63639904-e7b4-4984-b776-1672e402151a
  
  By default, any newly created files are not executable regardless of its file extension suffix. #flashcard
-
- id:: 63639904-7222-46cb-8b83-1a64c91386a8
  
  In fact, the file extension on GNU/Linux systems mostly does not have any meaning apart from the fact, that upon the execution of ls command to list all files and directories it is immediately clear that file with extension .sh is plausibly a shell script and file with .jpg is likely to be a lossy compressed image. #flashcard
-
- id:: 63639904-9a61-4059-ab92-d27f84c6c368
   How can you get the current user inside a script? #flashcard 
    user=$(whoami)
-
- id:: 63639904-6178-40dc-b89b-367bcd6decbb
   Different command outputs. #flashcard 
    The difference between stdout and stderr output is an essential concept as it allows us to a threat, that is, to redirect each output separately. The > notation is used to redirect stdout to a file whereas 2> notation is used to redirect stderr and &> is used to redirect both stdout and stderr.
-
- id:: 63639904-07d3-4235-a565-517c2f44caef
   Syntax of function. #flashcard 
    function total_files {
     find $1 -type f | wc -l
     }
-
- id:: 63639904-ba88-49d0-bae4-c29594301468
   if syntax #flashcard 
    if [ $num_a -lt $num_b ]; then
     echo "$num_a is less than $num_b!"
     fi
-
- id:: 63639904-4495-4a1b-a54c-c8071424badf
   How can you count the number of arguments passed? #flashcard 
    Using $# on Line 4, we are printing the total number of supplied arguments
-
- id:: 63639904-9a3d-4921-bd9d-98608a1f403d
   for syntax #flashcard 
    for i in 1 2 3; do
     echo $i
     done
-
- id:: 63639904-65dd-4fb3-a4a8-7515a16812a6
   while syntax #flashcard 
    counter=0
     while [ $counter -lt 3 ]; do
     let counter+=1
     echo $counter
     done
-
- id:: 63639904-f949-46f7-a8cb-3242d1a73dd8
   until syntax #flashcard 
    counter=6
     until [ $counter -lt 3 ]; do
     let counter-=1
     echo $counter
     done
-