title:: Bash Scripting Tutorial for Beginners - LinuxConfig.org (highlights)
deck:: [[Across-the-Net]]
author:: [[linuxconfig.org]]
full-title:: "Bash Scripting Tutorial for Beginners - LinuxConfig.org"
category:: #articles
url:: https://linuxconfig.org/bash-scripting-tutorial-for-beginners

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- What should be at the top of every script? #flashcard
		  id:: e061c014-6a8c-499f-8c81-b28ed3fd0a8a
			- all our scripts will include shell interpreter definition #!/bin/bash
	- -
	- -
		- How can we make our file executable? #flashcard
		  id:: 2f2274c3-245c-45c2-8695-adb83ef22d89
			- chmod +x FILENAME
	- -
	- -
		- By default, any newly created files are not executable regardless of its file extension suffix. #flashcard
		  id:: f6dd77fc-2014-42c7-84a0-abe2cba9fc37
	- -
	- -
		- In fact, the file extension on GNU/Linux systems mostly does not have any meaning apart from the fact, that upon the execution of ls command to list all files and directories it is immediately clear that file with extension .sh is plausibly a shell script and file with .jpg is likely to be a lossy compressed image. #flashcard
		  id:: 15b4b8f6-9e80-469c-ac07-15d9ecfb891b
	- -
	- -
		- How can you get the current user inside a script? #flashcard
		  id:: 1ca39955-dcc6-4d6f-88e8-a9ef44ecda64
			- user=$(whoami)
	- -
	- -
		- Different command outputs. #flashcard
		  id:: 9cfac383-3578-4d1b-a886-8970f622f902
			- The difference between stdout and stderr output is an essential concept as it allows us to a threat, that is, to redirect each output separately. The > notation is used to redirect stdout to a file whereas 2> notation is used to redirect stderr and &> is used to redirect both stdout and stderr.
	- -
	- -
		- Syntax of function. #flashcard
		  id:: 5a6f143f-b282-4b19-9c59-dad594037cd0
			- function total_files {
			        find $1 -type f | wc -l
			  }
	- -
	- -
		- if syntax #flashcard
		  id:: 3106a3c8-fe49-490b-94d8-7dbf04ccb2ac
			- if [ $num_a -lt $num_b ]; then
			    echo "$num_a is less than $num_b!"
			  fi
	- -
	- -
		- How can you count the number of arguments passed? #flashcard
		  id:: 54496c38-19b9-45e5-96e3-ca8511483c7b
			- Using $# on Line 4, we are printing the total number of supplied arguments
	- -
	- -
		- for syntax #flashcard
		  id:: ee088e3a-db3b-4a42-9146-e77a95f021c4
			- for i in 1 2 3; do
			    echo $i
			  done
	- -
	- -
		- while syntax #flashcard
		  id:: f029ebd0-e1ce-42c9-b53c-30b80edc1668
			- counter=0
			  while [ $counter -lt 3 ]; do
			    let counter+=1
			    echo $counter
			  done
	- -
	- -
		- until syntax #flashcard
		  id:: 06c175fb-935f-4f27-aec7-6f2d2d02b60e
			- counter=6
			  until [ $counter -lt 3 ]; do
			    let counter-=1
			    echo $counter
			  done
	- -