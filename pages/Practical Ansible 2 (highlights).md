title:: Practical Ansible 2 (highlights)
author:: [[]]
full-title:: "Practical Ansible 2"
category:: #books

tags:: #[[O'Reilly-Learning]]

- #tags #[[O'Reilly-Learning]]
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- Understanding how Ansible connects to hosts
		- -
		- [CODE] Do ping to a group of an inventory file with Ansible: #car
			- $ ansible webservers -m ping
		- -
	- Verifying the Ansible installation
		- -
		- [CODE] Display facts but with a filter: #car
		  id:: 6340152e-ba22-4d27-9124-4c018549cf0e
			- $ ansible frontends -i hosts -m setup -a "filter=ansible_distribution*"
		- -
		- -
		- [CODE] Display facts about your inventory: #car
		  id:: 6340152e-68bd-409e-99f2-d7b559abf2ca
			- $ ansible frontends -i hosts -m setup | less
		- -
		- -
		- [CODE] Do a ping to the target hosts: #car
		  id:: 6340152e-fa7d-469f-9f26-fe9a1bdfed66
			- $ ansible frontends -i hosts -m ping
		- -