title:: SSH-Copy-Id - Permission Denied (highlights)
author:: [[serverfault.com]]
full-title:: "SSH-Copy-Id - Permission Denied"
category:: #articles
url:: https://serverfault.com/questions/684346/ssh-copy-id-permission-denied-publickey

- Highlights first synced by [[Readwise]] [[Friday, 02-09-2022]]
	- -
	- Permission denied (publickey) is the remote SSH server saying "I only accept public keys as an authentication method, go away".
	  id:: 634545cd-c801-4696-ab08-7c090f07b496
	  
	  That's your main challenge: Getting onto the remote system. Once you can do that, you can upload your key:
	  
	  
	  Using ssh-copy-id - it will allow you to specify a different key if you're in the process of replacing your old one, for example.
	  Edit the remote user's ~/.ssh/authorized_keys to append your key manually. #flashcard
	- -