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
- id:: 63c669e2-dd72-4e55-869f-9e0e4da27a70
   Example of looping an array in bash #flashcard 
    for animal in "${animals[@]}" ; do
     printf '%s\n' "$animal"
     done
-
### Reading data line by line
- id:: 63c669e2-3645-4751-af47-cd04a1fd37c0
   How to read a file line by line in Bash [fcs is the name of the file!] #flashcard 
    while read -r name ; do
     printf '%s\n' "$name"
     printf 'https://en.wikipedia.org/wiki/%s\n' "${name// /_}"
     done < fcs
-
### Scripting methods
- id:: 63c669e2-eedf-4a78-9dc3-be849a47e882
  
  Sourcing the script means to use the Bash source command to read all of the commands in a script into the current shell session and run them there. A source command to read in a script such as hello.bash might look like this:
     bash$ source hello.bash
     Hello, bashuser! #flashcard
-
### Arguments to scripts
- id:: 63c669e2-b0a5-4f5b-a194-f63f29551ce9
   Dealing with parameters in Bash #flashcard 
    You can get the arguments as positional parameters with "$1", "$2", "$3", and so on
     You can dynamically get all of the positional parameters without having to count them with "$@"
     You can count the number of positional parameters if you need to with "$#"
-