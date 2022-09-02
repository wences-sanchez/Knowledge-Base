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
	- ## Module 2: Labs #Labs
		- ### Learning objectives: {{renderer :todomaster}}
			- DONE Install Ansible on the control node.
			- DONE Configure the `ansible` user on the control node for ssh shared key access to managed nodes. Do not use a passphrase for the key pair.
			  collapsed:: true
			  :LOGBOOK:
			  CLOCK: [2022-09-01 Thu 17:28:36]--[2022-09-01 Thu 17:41:15] =>  00:12:39
			  CLOCK: [2022-09-02 Fri 11:23:54]--[2022-09-02 Fri 12:02:41] =>  00:38:47
			  :END:
				- Solution:
				  collapsed:: true
					- [`$ ssh-copy-id` no funcionaba. Daba error de clave pública. Lo busqué en Internet y el problema era que las claves públicas no estaban --> no se podía conectar por ssh]
					-
					- `(wences@laptop)$ cat ~/.ssh/id_rsa.put`
					- *Copiar contenido en el portapapeles*
					- `(vagrant@vm)$ vi /home/vagrant/.ssh/authorized_keys`
					- *Pegar para añadir contenido del fichero anterior. Cerrar vi*
					- `(vagrant@vm)$ exit`
					- `(wences@laptop)$ ssh -p 2222 vagrant@127.0.0.1`
					- *I'm inside!*
			- DONE Create a simple Ansible inventory on the control node in `/home/ansible/inventory` containing `node1` and `node2`.
			  collapsed:: true
			  :LOGBOOK:
			  CLOCK: [2022-09-02 Fri 12:03:26]--[2022-09-02 Fri 12:11:47] =>  00:08:21
			  :END:
				- Solution:
				  collapsed:: true
					- Crear un fichero de inventario (*inventory* por ejemplo) y añadir 127.0.0.1:2222
			- DONE Configure sudo access for Ansible on `node1` and `node2` such that Ansible may use sudo for any command with no password prompt.
			  collapsed:: true
			  :LOGBOOK:
			  CLOCK: [2022-09-02 Fri 12:11:50]--[2022-09-02 Fri 13:09:37] =>  00:57:47
			  :END:
				- Work-around:
				  collapsed:: true
					- I have used an ad-hoc command with the **-u** option.
					- I have learned that I can pass arguments to an ad-hoc commands with the -a option --> `$ ansible -i inventory all -m command -a 'echo Hola mundo!' ` # o con comillas dobles y espacios separando clave valor con '='
					-
			- TODO Verify each managed node is able to be accessed by Ansible from the control node using the `ping` module. Redirect the output of a successful command to `/home/ansible/output`.
			  :LOGBOOK:
			  CLOCK: [2022-09-02 Fri 13:09:40]--[2022-09-02 Fri 13:23:12] =>  00:13:32
			  :END:
			- TODO Hacer lo mismo pero en los servidores de ACloudGuru
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