title:: How to Determine Why My Computer Crashed? (highlights)
author:: [[unix.stackexchange.com]]
full-title:: "How to Determine Why My Computer Crashed?"
category:: #articles
url:: https://unix.stackexchange.com/questions/38608/how-to-determine-why-my-computer-crashed

- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- Where can I find my Debian logs if my laptop has just crashed? #car
	  id:: 63401517-a4be-4a3c-8218-614b914ca0fe
		- You can find all messages in /var/log/syslog and in other /var/log/ files. Old messages are in /var/log/syslog.1, /var/log/syslog.2.gz etc. if logrotate is installed.
		  
		  However, if the kernel really locks up, the probability is low that you will find any related message.
		  
		  It could be, that only the X server locks up. In this case, you can usually still access the PC over network via ssh (if you have installed it). There is also the  Magic SysRq key to unRaw the keyboard such that the shortcuts you tried could work, too.
		- #[[linux]]
	- -