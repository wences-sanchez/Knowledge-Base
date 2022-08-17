tags:: #O'Reilly-Learning #Linux #Videos
#tags #O'Reilly-Learning #Linux #Videos

- ## Module 1: [[Linux Essential Commands]]
	- ### Lesson 1: [[Installing Linux]]
	  id:: 62f6461c-f1b4-4b0b-bd96-bf4458c0af3b
		- The FSF originated because Unix had become very expensive.
		- RedHat is the most successful linux distribution #Curiosities
			- Free Linux distribution based on RedHat are Rocky and Alma Linux
			- Oracle is also based on RedHat
		- Ubuntu is based on Debian
	- ---
	-
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
	- ---
	-
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
		- `/root`. The home directory for the *root* user (obviously protected)
		- `/run` is for temporary files that processes create dynamically in a private environment when needed
		- `/sys` is for managing hardware (an advanced directory)
		- `/tmp` is for temporary files. Is writeable by anybody.
		- `/usr` contains your programs and binaries.
			- If you write a script or anything you want to provide it on the system you should copy it to `/usr/local` (if it's a binary, preferably to `/usr/local/bin`)
		- `/var` is for stuff that is created dynamically.
			- In the `/var/log` directory, that's where your logging service **might** write files (*might* because nowadays those are found in **systemd-journald**)
		-
		- Linux Foundation is the organization who is behind and who is responsible of **all** Linux distributions.
		-
		- Regular users have write-access to **two** directories only:
			- `/home`
			- `/tmp`
				- That's why all the tutorial examples write in `/tmp`!!
		- If you use `$ ls -ld /<directory>`, you'll see properties and not contents of a directory
		- The **second** column in the output of `$ ls -l` is the number of **links** in the directory
		- About **wildcards**
			- Wildcards are also known as globbing
			- Some examples of wildcards:
				- `$ ls a*`
				- `$ ls a?*`
				- `$ ls a[nm]*`
				- `$ ls a[a-e]*`
				- `$ ls -d ???`
					- looks for the directories that have three characters as its name
			- The range function won't work for numbers if they are not in `{ }`.
				- The `[ ]` are only for wildcards, they will print nothing.
			- The `.` (in wildcards) will only match a dot, not any character like regex are used to match.
				- In this case, just the final dot for the extension file.
			- The `?` (in wildcards) does **not** match any previous character.
				- It just matches a single character **(any)**, but **one**
					- `$ ls t???` -> temp (if exists)
		- `$ cp -a` copies all (visible) files
			- You'll have to add `'./.*'` to `-a` to include hidden ones
		- `$ cp -R` copies all the files (including subdirectories)
		- It's recommended to use **absolute** paths to avoid confusion!!
		-
		- #### Lab
		  collapsed:: true
			- DONE Create a directory structure /tmp/files/pictures, /tmp/files/photos and /tmp/files/videos
			  :LOGBOOK:
			  CLOCK: [2022-08-13 Sat 11:59:16]--[2022-08-13 Sat 12:00:12] =>  00:00:56
			  :END:
			- DONE Copy all files that have a name starting with an a, b or c from /etc to /tmp/files
			  :LOGBOOK:
			  CLOCK: [2022-08-13 Sat 12:00:14]--[2022-08-13 Sat 12:01:48] =>  00:01:34
			  :END:
			- DONE From /tmp/files, move all files that have a name starting with an a or b to /tmp/files/photos, and files with a name starting with a c to /tmp/files/videos
			  :LOGBOOK:
			  CLOCK: [2022-08-13 Sat 12:01:50]--[2022-08-13 Sat 12:03:15] =>  00:01:25
			  :END:
	-
		- #### Flashcards
		  collapsed:: true
			- Explain each directory of the Linux hierarchy: #flashcard
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
				- `/root`. The home directory for the *root* user (obviously protected)
				- `/run` is for temporary files that processes create dynamically in a private environment when needed
				- `/sys` is for managing hardware (an advanced directory)
				- `/tmp` is for temporary files. Is writeable by anybody.
				- `/usr` contains your programs and binaries.
					- If you write a script or anything you want to provide it on the system you should copy it to `/usr/local` (if it's a binary, preferably to `/usr/local/bin`)
				- `/var` is for stuff that is created dynamically.
					- In the `/var/log` directory, that's where your logging service **might** write files (*might* because nowadays those are found in **systemd-journald**)
				-
				- Linux Foundation is the organization who is behind and who is responsible of **all** Linux distributions.
				-
				- Regular users have write-access to **two** directories only:
					- `/home`
					- `/tmp`
						- That's why all the tutorial examples write in `/tmp`!!
			- What does the symbol `?` mean in globbing? #flashcard
				- The `?` (in wildcards) does **not** match any previous character.
					- It just matches a single character **(any)**, but **one**
						- `$ ls t???` -> temp (if exists)
				- It's just one character
	- ---
	- ### Lesson 4: [[Advanced File Management Tools]]
		- #### 4.1 Understanding Hard and Symbolic Links
			- A link is a file system entry that refers to another file or directory
			- Hard links are pointing to the same inode on the same file system
			- Symbolic links are shortcuts and add additional flexibility
				- Symbolic links can exist on a directory
				- Cross-deviced ones are allowed
			- Every file Linux file system has an **inode**, and the inode contains complete administration of the file (but its name).
			- From the **inode**, a reference is made to the **blocks**.
			- The **blocks** are physical allocation unit on disc that a file is using.
			- A **hard link** points to the name of an **inode**.
			- A **symbolic link** (**NOT** ~~soft~~)
			- A **hard link** points to the inode itself, unlike a **symbolic link**, which points just to the name of the file
			- ![image.png](../assets/image_1660386646097_0.png)
		- #### 4.2 Managing Hard and Symbolic Links
			- You can use `$ ls */<your-file>` to easily find a file
			- If you configurate or modify one of the files, the others are modified too.
				- They are indeed the same file
			- It's a good idea to use **absolute** paths when creating symbolic links
			- The **second column of $ls** indicates the number of **hard links** that exist in the directory
		- #### 4.3 Finding Files with find #spaced
			- Examples:
				- `$ find / -name "hosts"`
				- `$ find / -name "hosts*"`
				- `$ find / -user linda`
				- `$ find / -size +2G`
				- `$ find / -user linda -exec cp {} /root/linda \;`
				- `$ find / -perm /4000`
			-
			- You shoud round the keyword with double quotes when using `$ find`
			- -exec has two parts:
				- The first command: For example: `cp {}`
				- and the second part: `/root/linda/ \;`
			- Why that trailing `\;` at the end of a find command?
				- The -exec option needs a semicolon to be included in its syntax.
				- But the shell reads that semicolon as a special character.
				- So we just scape it.
		- #### 4.4 Using Advanced find Options #spaced
			- Examples:
				- `$ find / -type f -size +1G`
				- `$ find /etc -exec grep -l student {} \; -exec cp {} find/contents/ \;`
				- `$ find /etc/ -name '*' -type f | xargs grep "127.0.0.1"`
				- `$ find /etc/ -name '*ini' -printf '%s, %p\n' | sort -rn`
				- `$ find / -name "student" -type f ! -path '*/proc/*' ! -path '*/tmp/*'`
			- You can search text inside every one of your files with:
				- `$ find / -exec grep "<keyword>" {} \;`
		- #### 4.5 Using which and locate #spaced
			- **find**  is very powerful, but also because of that, is somewhat slow.
			- **locate** is much faster. But works on a database that needs to be defined using **updatedb**
			- **which** is useful to find the exact location of binary files from the *$PATH* variable. For finding executables.
		- #### 4.6 Archiving Files with tar
			- **tar** is the Tape Archiver, and was created a long time ago
			- Usages (without compression):
				- `$ tar -cvf my_archive.tar /home`
				- `$ tar -xvf my_archive`
		- #### 4.7 Managing Files Compression
			- There exist other alternatives to *zip* like:
				- gzip
				- bzip2 (-j)
				- xzip (-J)
		- #### 4.8 Mounting File Systems #spaced
			- In order to **mount** the devices, we have to include them in the Linux **file structure**, because that won't change.
			- When we mount a device in (for example, `/dev/sda1`) the root directory, anything that you write to files somewhere in the root directory, will be written to this `/dev/sda1`
				- Another example: when you mount a `/dev/sdb1` device (a usb plug) in the `/mnt` directory, if you write files to the `/mnt` directory then really the files end up there on your `/dev/sdb1` device.
				- And at the moment you disconnect your `/dev/sdb1`device, the files that you've just written to it are gone, because the mount is no longer there. So the files will dissapear gone to that device.
				- You should type **umount** right before disconnecting your device
			- **$ lsblk** lists block devices
			- **$ mount** lists all current mounts (including administrative ones)
			- **$ df -h** presents mounted devices (including available disk space)
			- **$ findmnt** shows all mounts
		- #### Lab
		  collapsed:: true
			- DONE Find all files in `/etc` that have a size smaller than 1000 bytes and copy those to `/tmp/files/pictures`
			  collapsed:: true
			  :LOGBOOK:
			  CLOCK: [2022-08-16 Tue 10:21:16]--[2022-08-16 Tue 10:52:45] =>  00:31:29
			  :END:
				- Solution:
				  collapsed:: true
					- `$ sudo find /etc -size -1000c -exec cp {} /tmp/files/pictures` \\;
			- DONE In `/tmp/files`, create a symbolic link to `/var`
			  collapsed:: true
			  :LOGBOOK:
			  CLOCK: [2022-08-16 Tue 10:59:49]--[2022-08-16 Tue 11:01:24] =>  00:01:35
			  :END:
				- Solution:
				  collapsed:: true
					- `$ cd /tmp/files && ln -s /var var`
			- DONE Create a compressed archive file of the `/home` directory
			  collapsed:: true
			  :LOGBOOK:
			  CLOCK: [2022-08-16 Tue 11:01:26]--[2022-08-16 Tue 11:06:45] =>  00:05:19
			  :END:
				- Solution:
				  collapsed:: true
					- `$ tar -czvf home.tar.gz /home`
			- DONE Extract this compressed archive file with relative file names in `/tmp/archive`
			  collapsed:: true
			  :LOGBOOK:
			  CLOCK: [2022-08-16 Tue 11:06:47]--[2022-08-16 Tue 11:13:06] =>  00:06:19
			  CLOCK: [2022-08-16 Tue 11:13:09]--[2022-08-16 Tue 11:13:10] =>  00:00:01
			  :END:
				- Solution:
				  collapsed:: true
					- `$ tar -xfv /tmp/archive`
	-
		- #### Flashcards
			- Describe what is a link in Linux. #flashcard
			  collapsed:: true
				- A link is a file system entry that refers to another file or directory
				- Hard links are pointing to the same inode on the same file system
				- Symbolic links are shortcuts and add additional flexibility
					- Symbolic links can exist on a directory
					- Cross-deviced ones are allowed
				- Every file Linux file system has an **inode**, and the inode contains complete administration of the file (but its name).
				- From the **inode**, a reference is made to the **blocks**.
				- The **blocks** are physical allocation unit on disc that a file is using.
				- A **hard link** points to the name of an **inode**.
				- A **symbolic link** (**NOT** ~~soft~~)
				- A **hard link** points to the inode itself, unlike a **symbolic link**, which points just to the name of the file
				- ![image.png](../assets/image_1660386646097_0.png)
				- It's a good idea to use **absolute** paths when creating symbolic links
			- What means the second column (that number) in the output of the `$ ls -l` command? #flashcard
			  collapsed:: true
				- The **second column of $ls** indicates the number of **hard links** that exist in the directory
	- ---
	-
	- ### Lesson 5: [[Working with Text Files]] #spaced
		- In some systems, you'll only find **vi**.
			- That's the reason because it's preferred over *nano*
		- #### 5.2 Understanding Working with vim
			- If you want to replace some text, you use:
				- `:%s/old/new/g`
			- You should try **$ vimtutor**
		- #### 5.3 Creating Text Files with vim
			- You can use the shortcut SHIFT + Z Z to exit vim saving your file
		- #### 5.4 Browsing Text Files with more and less
			- **more** was the original file pager
				- In **more** there is no way of go backwards
			- **less** was developed to offer som more advanced features
			- **$ less -l** automatically update the file
		- #### 5.5 Using head and tail to see file start and end
			- `$ head -3 my-file`
				- will show only the first 3 lines of *my-file*
		- #### 5.6 Displaying File Contents with cat and tac
			- **cat** has some nice options
				- **-A** shows all non-printable characters
			- **tac** shows the files. But in reverse order!
		- #### 5.7 Working with grep
			- **grep** is used to search text strings or regular expressions in files (or using pipe in command output)
				- For example, `$ grep llinda *` searches text *linda* in all files in the current directory
				- With **-C<num>** it shows you the context before and after
		- #### Lab
		  collapsed:: true
			- DONE Use **vim** to create a text file **users** containing the following text:
			  :LOGBOOK:
			  CLOCK: [2022-08-16 Tue 13:48:49]--[2022-08-16 Tue 13:49:44] =>  00:00:55
			  :END:
				- anna
				  annabelle
				  bella
				  annna
				  belle anna
				  anna belle
			- DONE Use grep to filter all lines that contain the text anna
			  :LOGBOOK:
			  CLOCK: [2022-08-16 Tue 13:49:46]--[2022-08-16 Tue 13:50:37] =>  00:00:51
			  :END:
			- DONE Use the appropriate tool to print the last line only from this file
			  :LOGBOOK:
			  CLOCK: [2022-08-16 Tue 13:50:40]--[2022-08-16 Tue 13:51:41] =>  00:01:01
			  :END:
			- DONE Print the contents of this text file on-screen in reversed order
			  :LOGBOOK:
			  CLOCK: [2022-08-16 Tue 13:51:42]--[2022-08-16 Tue 13:51:58] =>  00:00:16
			  :END:
			-
			-
			-
	- ---
	-
	- ### Lesson 6: [[Advanced Text File Processing]] #spaced
		- **cut** filters out columns from text files
		- **sort** sorts the result (for example, from the **cut** command)
		- If the regex is an extended one, it won't always work!
		- There are different regex languages, so searching in Google might not work.
		- Table of regula expressions:
			- ![image.png](../assets/image_1660651484172_0.png)
		- You can use `\b` para referenciar un final de una palabra
		- It's a good idea to use the **-E** parameter of **grep**
		- You have to scape the `{ }` in your grep command
		-
		- It's almost mandatory to type `[:lower:]` and `[:upper:]` instead of a-z and A-Z because the latter won't work with many languages
		-
		- #### 6.4 An introduction to awk
			- `$ awk '{ print $0 }' /etc/passwd`
			- `$ awk [ -F <sep> ] '{ <awk-statement> }' file`
			- awk-statements:
				- print $0
				- length($0)
			- `$ awk -F : '/linda/ { print $3 }' /etc/passwd`
			-
		- #### 6.5 Getting Started with sed
			- `$ sed -i s/<to-remove>/<new>/g my-file`
			- `-i` is for input
			- `-g` is for global
			- Be aware that there is no undo!!
			-
		- #### Lab
		  collapsed:: true
			- DONE Lesson 6 Lab: Working with Text Files
			  :LOGBOOK:
			  CLOCK: [2022-08-16 Tue 17:08:27]--[2022-08-16 Tue 17:43:59] =>  00:35:32
			  :END:
				- DONE Use `sed` to display the fifth line of the file *users* that you created in Lesson 5 Lab
				  collapsed:: true
				  :LOGBOOK:
				  CLOCK: [2022-08-16 Tue 17:08:28]--[2022-08-16 Tue 17:21:37] =>  00:13:09
				  :END:
					- Solution:
					  collapsed:: true
						- `$ sed -n 5p users`
				- DONE Use `awk` in a pipe to filter the first column out of the results of the command `ps aux`
				  collapsed:: true
				  :LOGBOOK:
				  CLOCK: [2022-08-16 Tue 17:22:20]--[2022-08-16 Tue 17:25:41] =>  00:03:21
				  CLOCK: [2022-08-16 Tue 17:25:45]--[2022-08-16 Tue 17:25:46] =>  00:00:01
				  :END:
					- Solution:
					  collapsed:: true
						- `$ ps aux | awk '{ print $1 }'`
				- DONE Use `grep` to show the names of all files in `/etc` that have lines starting with the text *'root'*
				  collapsed:: true
				  :LOGBOOK:
				  CLOCK: [2022-08-16 Tue 17:25:48]--[2022-08-16 Tue 17:29:43] =>  00:03:55
				  :END:
					- Solution:
					  collapsed:: true
						- `$ grep -lr '^root' /etc/`
				- DONE Use `grep` to show all lines from all files in *users* that contain one or two letters `n`
				  collapsed:: true
				  :LOGBOOK:
				  CLOCK: [2022-08-16 Tue 17:29:46]--[2022-08-16 Tue 17:35:28] =>  00:05:42
				  :END:
					- Solution:
						- `$ grep 'n\{1,2\}' users`
				- DONE Use `grep` to find all files that contain the string "anna" where nothing occurs behind the string
				  collapsed:: true
				  :LOGBOOK:
				  CLOCK: [2022-08-16 Tue 17:37:03]--[2022-08-16 Tue 17:38:41] =>  00:01:38
				  :END:
					- Solution:
					  collapsed:: true
						- `$ grep 'anna.' users`
						- `$ grep -R 'anna$' users`
						-
	- ---
	-
	- ### Lesson 7: [[Connecting to a Server]]
		- The **root** user exists in Linux kernel space.
		- Linux distros either remove any root or fence it.
		- The best alternative is to use **sudo**
		-
		- **su** is for Switch User, it allows you to open a shell as a specific user.
		- Use **su** to open a subshell, not all environment variables are set as the target user
		- Use **su -** to open a login shell, environment variables are set as the target user
		-
		- **sudo** is a more sophisticated way, preferred.
		- ![image.png](../assets/image_1660668276842_0.png)
		-
		- The fingerprint is the identity.
		-
	- ---
		- ### Lesson 8: [[Working with the Bash Shell]]
			- The `&>` sends both file descriptors 1 and 2 to the specified output
			- #### 8.3 Working with history
				- Commands a user types are written to `~/.bash_history`
					- **$ history** shows the last commands you wrote
				- Use:
					- **$ history -c** to clear the current history
					- **$ history -w** to write the current history
					- **$ history -d** to delete a specific line from history
				- And use:
					- **Ctrl-r** for reverse-i-search
					- **$ !nn** to execute that line command from history
			- #### Bash is case-sensitive
			- #### /home/wences/.local/bin is a bin directory included directory!!!
			-
		-
			- #### Flashcards
				- How could you send (in Linux) both file descriptors 1 and 2 to the specified output? #flashcard
					- With `&>`
			-
-
-
-
-
-