title:: Ansible (highlights)
deck:: [[O'Reilly-Learning::Ansible]]
author:: [[Michael Heap]]
full-title:: "Ansible"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- 1. Getting Started
		- -
			- How to use multiple items in Ansible inside an apt task. #flashcard
			  id:: 9a3241e6-0821-45c6-ab7b-1e3268694da1
				- name: Install required packages
				      apt: name={{item}} state=present update_cache=yes
				      with_items:
				        - php5-cli
				        - nginx
				        - mysql-server-5.6
		- -
		- -
			- The Ansible documentation for playbooks is excellent, and it should always be your first point of reference for playbook syntax ( http://docs.ansible.com/ansible/index.html ).
			  id:: e534724b-70cf-487c-80ac-e31f9fa4d4e6
			  
			  If you want to jump straight in and see some sample playbooks, there are lots of them available in the ansible-examples repository on Github ( https://github.com/ansible/ansible-examples ). #flashcard
		- -
	- 7. Orchestrating AWS
		- -
			- About orchestration and provisioning types of playbooks in Ansible. #flashcard
			  id:: 8a4ab22d-9d81-42b4-a563-88fd411b815b
				- Ansible playbooks can be categorized as one of two types of playbook: orchestration or provisioning . Up until this point, you’ve been writing provisioning playbooks that log in to a remote machine and configure it using the information defined in the playbook. This new playbook is the other kind—an orchestration playbook. An orchestration playbook does not connect to any remote machines to perform its tasks. Instead, it runs everything on your local machine. This is because orchestration playbooks tend to use public APIs to accomplish their work rather than running shell commands against a remote machine.
				  
				  As this is an orchestration playbook and you don’t have a remote machine to connect to, you should add connection: local to your playbook. This tells Ansible that it should run on the local machine instead of trying to SSH to a remote machine (as there isn’t one available). We do this because the AWS modules in Ansible do not run against a remote host. Instead, they make HTTP requests to the Amazon API to perform actions such as creating a virtual machine.
		- -