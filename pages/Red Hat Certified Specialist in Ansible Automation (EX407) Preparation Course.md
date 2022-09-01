title:: Red Hat Certified Specialist in Ansible Automation (EX407) Preparation Course
tags:: ACloudGuru, Ansible

- #tags #ACloudGuru #Ansible
-
- ## Module 1: [[Red Hat Certified Specialist in Ansible Automation (EX407) Preparation Course/Course Overview]]
-
- ## Module 2: [[Red Hat Certified Specialist in Ansible Automation (EX407) Preparation Course/Understanding Core Components of Ansible]]
	- ### Inventories
		- **Inventories** are how Ansible locate and run against multiple systems.
		- You can think of an inventory as a list of hosts
		- Inventories are located in `/etc/ansible/hosts`, but that is configurable
		- It could be formatted as an INI file or as a YAML file
	-
		- When you are in the CLI, you have to specify the hosts against the control node will run and the module (with **-m**). It could be a built-in module.
			- You can specify a custom inventory of yours (instead of the default) with the **-i** option.
	- #### Flashcards
	  collapsed:: true
		- Talk about *inventories* in Ansible, how do we deal with them and where they are. Also how they are called. #flashcard
			- **Inventories** are how Ansible locate and run against multiple systems.
			- You can think of an inventory as a list of hosts
			- Inventories are located in `/etc/ansible/hosts`, but that is configurable
			- It could be formatted as an INI file or as a YAML file
			-
				- When you are in the CLI, you have to specify the hosts against the control node will run and the module (with **-m**). It could be a built-in module.
					- You can specify a custom inventory of yours (instead of the default) with the **-i** option.
		-
	- ### Modules
		- **Modules** are essentially tools for particular tasks
		- **Modules** (usually) take parameters
		- They can run from the comamnd line or within a playbook
		- There are a significant number of modules for many kinds of work
		-
	- ### Variables
		- Typically used for configuration values and various parameters
		- Ansible variables may also be dictionaries.
	-
	- ### Facts
		- Facts provide certain information about a given target host.
		- Facts are discovered by Ansible automatically when it reaches out to a host
			- Fact gathering may be disabled
			- It can be slow, but it retrieves the facts at that time and if you use variables you should use it.
	- #### Flashcards
	  collapsed:: true
		- About modules, variables and facts (when are facts caught?) #flashcard
			- ### Modules
				- **Modules** are essentially tools for particular tasks
				- **Modules** (usually) take parameters
				- They can run from the comamnd line or within a playbook
				- There are a significant number of modules for many kinds of work
				-
			- ### Variables
				- Typically used for configuration values and various parameters
				- Ansible variables may also be dictionaries.
			-
			- ### Facts
				- Facts provide certain information about a given target host.
				- Facts are discovered by Ansible automatically when it reaches out to a host
					- Fact gathering may be disabled
					- It can be slow, but it retrieves the facts at that time and if you use variables you should use it.
	- ### Plays and Playbooks
		- The goal of a **play** is to map a group of hosts to some well-defined **roles**
		- A **play** may use one or more modules to achieve a desired state on a **group of hosts**
		- A **playbook** is a series of **plays**
		- A **playbook** may deploy new web servers, install a new application to existing application servers, and run SQL against some database servers to support the new application.
	-
	- #### Flashcards
	  collapsed:: true
		- About plays and playbooks #flashcard
			- The goal of a **play** is to map a group of hosts to some well-defined **roles**
			- A **play** may use one or more modules to achieve a desired state on a **group of hosts**
			- A **playbook** is a series of **plays**
			- A **playbook** may deploy new web servers, install a new application to existing application servers, and run SQL against some database servers to support the new application.
	- ### Configuration Files
		- Several possible locations (in order processed):
			- 1. ANSIBLE_CONFIG (an environment variable)
			  2. ansible.cfg (in the current directory)
			  3. .ansible.cfg (in the home directory)
			  4. /etc/ansible/ansible.cfg
			- If one found, the process stops.
		- Configuration can also be set in environment variables
		-
	- ### Ansible Configuration File
		- It's in `/etc/ansible/ansible.cfg`
		- You should read the file comprehensively and make little edits in it.
	-
	- #### Flashcards
		- Where can the configuration files be located in Ansible? #flashcard
			- Several possible locations (in order processed):
				- 1. ANSIBLE_CONFIG (an environment variable)
				  2. ansible.cfg (in the current directory)
				  3. .ansible.cfg (in the home directory)
				  4. /etc/ansible/ansible.cfg
				- If one found, the process stops.
			- Configuration can also be set in environment variables
			- You should read the file comprehensively and make little edits in it.
		-
		- Las variables de Ansible, ¿pueden ser globales, de alguna manera? #flashcard
			- Sí, puedes definir variables para un solo grupo de hosts, por ejemplo.
				- Puedes definirla para el grupo *default*, y así sería global a todos los hosts.
			- También puedes usar variables de entorno del sistema como variables globales.
		- Si uso una variable en un play, ¿será esta global? :: No, estará limitada al play y no podrá usarse fuera ni en el mismo playbook.
		- Ansible variables, are they global? #flashcard
			- Short answer: yes
			- Long answer: they can be scoped to specific groups and hosts.
			-
		-
		- What is the goal of an Ansible play? #flashcard
			- To map a group of hosts to some well-defined roles
		- Where is the Ansible inventory stored by default? #flashcard
			- In `/etc/ansible/hosts`
			- #flashcard
-
- ## Module 1:Labs #Labs
	- ### Learning objectives:
		- DONE Install Ansible on the control node.
		- DOING Configure the `ansible` user on the control node for ssh shared key access to 
		  :LOGBOOK:
		  CLOCK: [2022-09-01 Thu 17:28:36]
		  :END:
		  managed nodes. Do not use a passphrase for the key pair.
		- TODO Create a simple Ansible inventory on the control node in `/home/ansible/inventory` containing `node1` and `node2`.
		- TODO Configure sudo access for Ansible on `node1` and `node2` such that Ansible may use sudo for any command with no password prompt.
		- TODO Verify each managed node is able to be accessed by Ansible from the control node using the `ping` module. Redirect the output of a successful command to `/home/ansible/output`.
-
-
-
-
-
-
-
-
-
-
-
-
-
-
-