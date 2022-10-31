title:: Bash Quick Start Guide (highlights)
deck:: [[O'Reilly-Learning::Bash Quick Start Guide]]
author:: [[]]
full-title:: "Bash Quick Start Guide"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Saving fields into arrays
		- -
		- for animal in "${animals[@]}" ; do
		        printf '%s\n' "$animal"
		    done #flashcard
			- Example of looping an array in bash
		- -
	- Reading data line by line
		- -
		- while read -r name ; do
		    printf '%s\n' "$name"
		    printf 'https://en.wikipedia.org/wiki/%s\n' "${name// /_}"
		  done < fcs #flashcard
			- How to read a file line by line in Bash [fcs is the name of the file!]
		- -
	- Scripting methods
		- -
		- Sourcing the script means to use the Bash source command to read all of the commands in a script into the current shell session and run them there. A source command to read in a script such as hello.bash might look like this:
		  bash$ source hello.bash
		  Hello, bashuser! #flashcard
		- -
	- Arguments to scripts
		- -
		- You can get the arguments as positional parameters with "$1", "$2", "$3", and so on
		  You can dynamically get all of the positional parameters without having to count them with "$@"
		  You can count the number of positional parameters if you need to with "$#" #flashcard
			- Dealing with parameters in Bash
		- -