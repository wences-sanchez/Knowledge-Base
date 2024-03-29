title:: Bash Quick Start Guide (highlights)
deck:: [[O'Reilly-Learning::Bash Quick Start Guide]]
author:: [[]]
full-title:: "Bash Quick Start Guide"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Saving fields into arrays
		- -
			- Example of looping an array in bash #flashcard
			  id:: 77570771-5451-478d-bdba-2c2ac49c6e25
				- for animal in "${animals[@]}" ; do
				        printf '%s\n' "$animal"
				    done
		- -
	- Reading data line by line
		- -
			- How to read a file line by line in Bash [fcs is the name of the file!] #flashcard
			  id:: 0bd1f964-d2f6-4b4e-b7f4-3628e6304b73
				- while read -r name ; do
				    printf '%s\n' "$name"
				    printf 'https://en.wikipedia.org/wiki/%s\n' "${name// /_}"
				  done < fcs
		- -
	- Scripting methods
		- -
			- Sourcing the script means to use the Bash source command to read all of the commands in a script into the current shell session and run them there. A source command to read in a script such as hello.bash might look like this:
			  id:: 754af07d-ccc7-4668-afe1-55fa83e2c755
			  bash$ source hello.bash
			  Hello, bashuser! #flashcard
		- -
	- Arguments to scripts
		- -
			- Dealing with parameters in Bash #flashcard
			  id:: 936727b5-f7c3-4dee-a75e-6b36d75796c6
				- You can get the arguments as positional parameters with "$1", "$2", "$3", and so on
				  You can dynamically get all of the positional parameters without having to count them with "$@"
				  You can count the number of positional parameters if you need to with "$#"
		- -