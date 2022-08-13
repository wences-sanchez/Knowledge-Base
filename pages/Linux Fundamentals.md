tags:: #O'Reilly-Learning #Linux #Videos
#tags #O'Reilly-Learning #Linux #Videos

- ## Module 1: [[Essential Commands]]
	- ### Lesson 1: [[Installing Linux]]
	  id:: 62f6461c-f1b4-4b0b-bd96-bf4458c0af3b
		- The FSF originated because Unix had become very expensive.
		- RedHat is the most successful linux distribution #Curiosities
			- Free Linux distribution based on RedHat are Rocky and Alma Linux
			- Oracle is also based on RedHat
		- Ubuntu is based on Debian
	- ### Lesson 2: [[Using Essential Tools]] #spaced
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
		  collapsed:: true
			- DONE Use **man** and related resources to find out how to change the **hostname** of your computer
			  collapsed:: true
			  :LOGBOOK:
			  CLOCK: [2022-08-12 Fri 14:34:36]--[2022-08-12 Fri 14:37:11] =>  00:02:35
			  CLOCK: [2022-08-12 Fri 14:37:12]--[2022-08-12 Fri 14:37:14] =>  00:00:02
			  :END:
				- `$ sudo hostname <new_name>`
			- DONE Read the help output for **ip** and find how you can bring down a **link**
			  collapsed:: true
			  :LOGBOOK:
			  CLOCK: [2022-08-12 Fri 14:37:26]--[2022-08-12 Fri 14:52:40] =>  00:15:14
			  :END:
				- I didn't fully understand the task :(
				- Solution:
				  collapsed:: true
					- `$ sudo ip link set <network_device> down`
					-
	-
		- #### Flashcards
			- How can you open a shell as another user? #flashcard
			  collapsed:: true
				- `$ su - [<user>]` can be used to open a shell as another user.
					- When used without arguments, a  root shell is opened after entering the root password
					- When used with a username as argument, a user shell is opened.
	- ### Lesson 3: [[Essential File Management Tools]]
	  id:: 62f66ba7-794b-4605-a7dc-145760843477
		- `/usr` is for your program files
		- `/var` is the directory that different services use to dynamically create files.
			- `/var/log` contains your log files and
			- `/var/cache` contains anything needed to be cached
		- `/etc` contains your configuration files
		- `/bin` stands for binary. And, in Linux, a binary is a command, a command file, a program file that can be used by ordinary users.
			- `/sbin` is a system binary. You need sudo privileges in order to use that.
			- `/bin` now points to `/usr/bin`. So, nowadays, the `/bin` directory doesn't have a function anymore and everything is now stored in `/usr/bin`
		- `/lib` and `/lib64` include libraries belonging to the files in `/bin` and `/sbin`
		- `/boot` contains everything that you need to boot.
		- `/dev` is where you'll find devices.
			- Devices is what allows you to access your hardware.
		- `/home` is the own user directory
		- `/media` and `/mnt` are for mounting stuff
		- `/opt` is an optional directory (not always used)
		- `/proc` provides an interface to what the kernel is doing.
		- `/root`. The home directory for
		- Linux Foundation is the organization who is behind and who is responsible of **all** Linux distributions.
		-
		- Regular users have write-access to **two** directories only:
			- `/home`
			- `/tmp`
				- That's why all the tutorial examples write in `/tmp`!!
		-