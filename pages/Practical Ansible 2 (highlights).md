title:: Practical Ansible 2 (highlights)
deck:: [[O'Reilly-Learning::Practical Ansible 2]]
author:: [[]]
full-title:: "Practical Ansible 2"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Understanding how Ansible connects to hosts
		- -
			- [CODE] Do ping to a group of an inventory file with Ansible: #flashcard
			  id:: 26178e6b-531e-4003-b9a7-a38432aa879d
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
			  id:: 6c6509b8-2ef6-48ce-b3cb-f4ae6a3a1446
				- $ ansible frontends -i hosts -m ping
		- -