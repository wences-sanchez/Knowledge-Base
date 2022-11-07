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
			  id:: 8574f8eb-f3e0-4418-b545-4a9be737556c
				- $ ansible frontends -i hosts -m setup -a "filter=ansible_distribution*"
		- -
		- -
			- [CODE] Display facts about your inventory: #flashcard
			  id:: a16cc2ec-cb7c-408c-b4b6-dd681b5e986e
				- $ ansible frontends -i hosts -m setup | less
		- -
		- -
			- [CODE] Do a ping to the target hosts: #flashcard
			  id:: 6c6509b8-2ef6-48ce-b3cb-f4ae6a3a1446
				- $ ansible frontends -i hosts -m ping
		- -