title:: Practical Ansible 2 (highlights) (1)
author:: [[]]
full-title:: "Practical Ansible 2"
category:: #books

tags:: O'Reilly-Learning

- #tags #O'Reilly-Learning
- Highlights first synced by [[Readwise]] [[Friday, 07-10-2022]]
	- Understanding how Ansible connects to hosts
		- -
		- [CODE] Do ping to a group of an inventory file with Ansible: #flashcard
			- $ ansible webservers -m ping
		- -
	- Verifying the Ansible installation
		- -
		- [CODE] Display facts but with a filter: #flashcard
			- $ ansible frontends -i hosts -m setup -a "filter=ansible_distribution*"
		- -
		- -
		- [CODE] Display facts about your inventory: #flashcard
			- $ ansible frontends -i hosts -m setup | less
		- -
		- -
		- [CODE] Do a ping to the target hosts: #flashcard
			- $ ansible frontends -i hosts -m ping
		- -