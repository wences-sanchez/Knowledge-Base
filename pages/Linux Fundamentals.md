tags:: #O'Reilly-Learning #Linux #Videos

- ## Module 1: [[Essential Commands]]
	- ### Lesson 1: [[Installing Linux]]
	  id:: 62f6461c-f1b4-4b0b-bd96-bf4458c0af3b
		- The FSF originated because Unix had become very expensive.
		- RedHat is the most successful linux distribution
			- Free Linux distribution based on RedHat are Rocky and Alma Linux
			- Oracle is also based on RedHat
		- Ubuntu is based on Debian
	- ### Lesson 2: [[Using Essential Tools]]
	  id:: 62f6387f-8424-416c-9a84-e9c46f041769
		- Use root is an alternative to sudo.
			- Root is dangerous. You shouldn't use that directly
		- I you are a user belonging to wheel or sudo, you can use sudo to run commands with administrator privileges.
		- Alternative, `$ su -` can be used to open a shell as another user.
			- When used without arguments, a  root shell is opened after entering the root password
			- When used with a username as argument, a user shell is opened.
		- `$ sudo` allows authorized users to run tasks with escalated privileges
			- But to use it, you have to be a member of the sudo (or wheel) group
		- The network interface *lo* is for **loopback**
		- The file **/etc/hosts** is for hosts resolution
		- The command `$ history` shows **a list** of your last typed **commands**
		- `$ pinfo` is another way of viewing the info contents.
		- `$ tldr` could contain (if any) examples of the command passed as a parameter
		- `/usr/share/doc/` directory contains some (maybe) useful information
		- #### Lab
			- DOING Use **man** and related resources to find out how to change the **hostname** of your computer
			  :LOGBOOK:
			  CLOCK: [2022-08-12 Fri 14:34:36]
			  :END:
				- `$ sudo hostname <new_name>`
			- TODO Read the help output for **ip** and find howe you can bring down a **link**
			-
		-
		-
		-
		-