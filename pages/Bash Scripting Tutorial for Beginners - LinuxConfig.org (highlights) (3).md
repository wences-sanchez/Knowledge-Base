title:: Bash Scripting Tutorial for Beginners - LinuxConfig.org (highlights) (3)
author:: [[Lubos Rendek]]
full-title:: "Bash Scripting Tutorial for Beginners - LinuxConfig.org"
category:: #articles
url:: https://linuxconfig.org/bash-scripting-tutorial-for-beginners

- Highlights first synced by [[Readwise]] [[Friday, 07-10-2022]]
	- -
	- What should be at the top of every script? #flashcard
		- all our scripts will include shell interpreter definition #!/bin/bash
	- -
	- -
	- How can we make our file executable? #flashcard
		- chmod +x FILENAME
	- -
	- -
	- By default, any newly created files are not executable regardless of its file extension suffix. #spaced
	- -
	- -
	- In fact, the file extension on GNU/Linux systems mostly does not have any meaning apart from the fact, that upon the execution of ls command to list all files and directories it is immediately clear that file with extension .sh is plausibly a shell script and file with .jpg is likely to be a lossy compressed image. #spaced
	- -
	- -
	- How can you get the current user inside a script? #flashcard
		- user=$(whoami)
	- -
	- -
	- Different command outputs. #flashcard
		- The difference between stdout and stderr output is an essential concept as it allows us to a threat, that is, to redirect each output separately. The > notation is used to redirect stdout to a file whereas 2> notation is used to redirect stderr and &> is used to redirect both stdout and stderr.
	- -
	- -
	- Syntax of function. #flashcard
		- function total_files {
		        find $1 -type f | wc -l
		  }
	- -
	- -
	- if syntax #flashcard
		- if [ $num_a -lt $num_b ]; then
		    echo "$num_a is less than $num_b!"
		  fi
	- -
	- -
	- How can you count the number of arguments passed? #flashcard
		- Using $# on Line 4, we are printing the total number of supplied arguments
	- -
	- -
	- for syntax #flashcard
		- for i in 1 2 3; do
		    echo $i
		  done
	- -
	- -
	- while syntax #flashcard
		- counter=0
		  while [ $counter -lt 3 ]; do
		    let counter+=1
		    echo $counter
		  done
	- -
	- -
	- until syntax #flashcard
		- counter=6
		  until [ $counter -lt 3 ]; do
		    let counter-=1
		    echo $counter
		  done
	- -