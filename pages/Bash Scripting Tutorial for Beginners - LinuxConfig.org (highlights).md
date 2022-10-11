title:: Bash Scripting Tutorial for Beginners - LinuxConfig.org (highlights)
author:: [[linuxconfig.org]]
full-title:: "Bash Scripting Tutorial for Beginners - LinuxConfig.org"
category:: #articles
url:: https://linuxconfig.org/bash-scripting-tutorial-for-beginners

- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- What should be at the top of every script? #car
	  id:: 634014f6-80f1-4b25-8cec-2ae09498c094
		- all our scripts will include shell interpreter definition #!/bin/bash
	- -
	- -
	- How can we make our file executable? #car
		- chmod +x FILENAME
	- -
	- -
	- By default, any newly created files are not executable regardless of its file extension suffix. #ñspace
	- -
	- -
	- In fact, the file extension on GNU/Linux systems mostly does not have any meaning apart from the fact, that upon the execution of ls command to list all files and directories it is immediately clear that file with extension .sh is plausibly a shell script and file with .jpg is likely to be a lossy compressed image. #ñspace
	- -
	- -
	- How can you get the current user inside a script? #car
	  id:: 634014f6-94b4-4162-9cd1-64ec27f2307b
		- user=$(whoami)
	- -
	- -
	- Different command outputs. #car
		- The difference between stdout and stderr output is an essential concept as it allows us to a threat, that is, to redirect each output separately. The > notation is used to redirect stdout to a file whereas 2> notation is used to redirect stderr and &> is used to redirect both stdout and stderr.
	- -
	- -
	- Syntax of function. #car
		- function total_files {
		        find $1 -type f | wc -l
		  }
	- -
	- -
	- if syntax #car
	  id:: 634014f6-f836-4234-9f73-a38cccd79bcd
		- if [ $num_a -lt $num_b ]; then
		    echo "$num_a is less than $num_b!"
		  fi
	- -
	- -
	- How can you count the number of arguments passed? #car
		- Using $# on Line 4, we are printing the total number of supplied arguments
	- -
	- -
	- for syntax #car
	  id:: 634014f6-554b-4fcd-a6b5-838503abc4e0
		- for i in 1 2 3; do
		    echo $i
		  done
	- -
	- -
	- while syntax #car
	  id:: 634014f6-f804-452c-a845-f0c1ea58a8ed
		- counter=0
		  while [ $counter -lt 3 ]; do
		    let counter+=1
		    echo $counter
		  done
	- -
	- -
	- until syntax #car
		- counter=6
		  until [ $counter -lt 3 ]; do
		    let counter-=1
		    echo $counter
		  done
	- -