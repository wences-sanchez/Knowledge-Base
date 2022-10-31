title:: Practical Ansible 2 (highlights)
deck:: [[O'Reilly-Learning::Practical Ansible 2]]
author:: [[]]
full-title:: "Practical Ansible 2"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- Understanding how Ansible connects to hosts
		- -
		- $ ansible webservers -m ping #flashcard
			- [CODE] Do ping to a group of an inventory file with Ansible:
		- -
	- Verifying the Ansible installation
		- -
		- $ ansible frontends -i hosts -m setup -a "filter=ansible_distribution*" #flashcard
			- [CODE] Display facts but with a filter:
		- -
		- -
		- $ ansible frontends -i hosts -m setup | less #flashcard
			- [CODE] Display facts about your inventory:
		- -
		- -
		- $ ansible frontends -i hosts -m ping #flashcard
			- [CODE] Do a ping to the target hosts:
		- -