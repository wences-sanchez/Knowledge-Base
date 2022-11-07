# Bash Quick Start Guide

deck:: [[O'Reilly-Learning::Bash Quick Start Guide]]\
author:: [[None]]\
full-title:: "Bash Quick Start Guide"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/bash-quick-start/9781789538830/ibis_generated_cover_thumbnail.jpg)
## Highlights
### Saving fields into arrays
- id:: 6363990d-1240-4ec8-83aa-25cbf82cc92d
   Example of looping an array in bash #flashcard 
    for animal in "${animals[@]}" ; do
     printf '%s\n' "$animal"
     done
-
### Reading data line by line
- id:: 6363990d-c460-461c-9986-9fcb971f3ee5
   How to read a file line by line in Bash [fcs is the name of the file!] #flashcard 
    while read -r name ; do
     printf '%s\n' "$name"
     printf 'https://en.wikipedia.org/wiki/%s\n' "${name// /_}"
     done < fcs
-
### Scripting methods
- id:: 6363990d-fe4c-40b3-b9ad-92aeea41d842
  
  Sourcing the script means to use the Bash source command to read all of the commands in a script into the current shell session and run them there. A source command to read in a script such as hello.bash might look like this:
     bash$ source hello.bash
     Hello, bashuser! #flashcard
-
### Arguments to scripts
- id:: 6363990d-d08a-466b-a314-c4ce5928acd5
   Dealing with parameters in Bash #flashcard 
    You can get the arguments as positional parameters with "$1", "$2", "$3", and so on
     You can dynamically get all of the positional parameters without having to count them with "$@"
     You can count the number of positional parameters if you need to with "$#"
-