title:: Ansible (highlights)
author:: [[Michael Heap]]
full-title:: "Ansible"
category:: #books

tags:: #[[O'Reilly-Learning]]

- #tags #[[O'Reilly-Learning]]
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- 1. Getting Started
		- -
		- How to use multiple items in Ansible inside an apt task. #card
			- name: Install required packages
			      apt: name={{item}} state=present update_cache=yes
			      with_items:
			        - php5-cli
			        - nginx
			        - mysql-server-5.6
		- -
		- -
		- The Ansible documentation for playbooks is excellent, and it should always be your first point of reference for playbook syntax ( http://docs.ansible.com/ansible/index.html ).
		  
		  If you want to jump straight in and see some sample playbooks, there are lots of them available in the ansible-examples repository on Github ( https://github.com/ansible/ansible-examples ). #space
		- -
	- 7. Orchestrating AWS
		- -
		- About orchestration and provisioning types of playbooks in Ansible. #card
			- Ansible playbooks can be categorized as one of two types of playbook: orchestration or provisioning . Up until this point, you’ve been writing provisioning playbooks that log in to a remote machine and configure it using the information defined in the playbook. This new playbook is the other kind—an orchestration playbook. An orchestration playbook does not connect to any remote machines to perform its tasks. Instead, it runs everything on your local machine. This is because orchestration playbooks tend to use public APIs to accomplish their work rather than running shell commands against a remote machine.
			  
			  As this is an orchestration playbook and you don’t have a remote machine to connect to, you should add connection: local to your playbook. This tells Ansible that it should run on the local machine instead of trying to SSH to a remote machine (as there isn’t one available). We do this because the AWS modules in Ansible do not run against a remote host. Instead, they make HTTP requests to the Amazon API to perform actions such as creating a virtual machine.
		- -
- New highlights added [[Thursday, 01-09-2022]] at 6:01 PM
	- 3. Inventory: Describing Your Servers
		- -
		- [Figure 3.2](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781098109141/files/assets/aur3_0302.png) #card
			- To sum up, a playbook contains one or more plays. A play associates an unordered set of hosts with an ordered list of tasks. Each task is associated with exactly one module. Figure 3-2 depicts the relationships between playbooks, plays, hosts, tasks, and modules.
		- -
	- 4. Variables and Facts
		- -
		- If the inventory file is marked executable, Ansible will assume it is a dynamic inventory script and will execute the file instead of reading it. #space
		- -