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
- 
 Example of looping an array in bash #flashcard 
    for animal in "${animals[@]}" ; do
     printf '%s\n' "$animal"
     done

    
-
### Reading data line by line
- 
 How to read a file line by line in Bash [fcs is the name of the file!] #flashcard 
    while read -r name ; do
     printf '%s\n' "$name"
     printf 'https://en.wikipedia.org/wiki/%s\n' "${name// /_}"
     done < fcs

    
-
### Scripting methods
- 

Sourcing the script means to use the Bash source command to read all of the commands in a script into the current shell session and run them there. A source command to read in a script such as hello.bash might look like this:
     bash$ source hello.bash
     Hello, bashuser! #flashcard 


    
-
### Arguments to scripts
- 
 Dealing with parameters in Bash #flashcard 
    You can get the arguments as positional parameters with "$1", "$2", "$3", and so on
     You can dynamically get all of the positional parameters without having to count them with "$@"
     You can count the number of positional parameters if you need to with "$#"

    
-
