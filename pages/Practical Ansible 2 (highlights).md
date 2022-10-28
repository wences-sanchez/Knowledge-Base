title:: Practical Ansible 2 (highlights)
author:: [[]]
full-title:: "Practical Ansible 2"
category:: #books

tags:: #[[O'Reilly-Learning]]

- Highlights first synced by [[Readwise]] [[Friday, 28-10-2022]]
	- Understanding how Ansible connects to hosts
		- $ ansible webservers -m ping
			- **Note**: [CODE] Do ping to a group of an inventory file with Ansible:
	- Verifying the Ansible installation
		- $ ansible frontends -i hosts -m setup -a "filter=ansible_distribution*"
			- **Note**: [CODE] Display facts but with a filter:
		- $ ansible frontends -i hosts -m setup | less
			- **Note**: [CODE] Display facts about your inventory:
		- $ ansible frontends -i hosts -m ping
			- **Note**: [CODE] Do a ping to the target hosts: