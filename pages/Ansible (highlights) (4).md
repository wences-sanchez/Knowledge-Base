title:: Ansible (highlights) (4)
author:: [[]]
full-title:: "Ansible"
category:: #books

tags:: O'Reilly-Learning

- #tags #O'Reilly-Learning
- Highlights first synced by [[Readwise]] [[Friday, 07-10-2022]]
	- 1. Introduction
		- -
		- in the playbook would look something like this:
		- -
		- -
		- Push-based
		  Chef and Puppet are configuration management systems that use agents. They are pull-based by default. Agents installed on the servers periodically check in with a central service and download configuration information from the service. Making configuration management changes to servers goes something like this:
		  
		  You: make a change to a configuration management script.
		  
		  You: push the change up to a configuration management central service.
		  
		  Agent on server: wakes up after periodic timer fires.
		  
		  Agent on server: connects to configuration management central service.
		  
		  Agent on server: downloads new configuration management scripts.
		  
		  Agent on server: executes configuration management scripts locally that change server state.
		  
		  In contrast, Ansible is push-based by default. Making a change looks like this:
		  
		  You: make a change to a playbook.
		  
		  You: run the new playbook.
		  
		  Ansible: connects to servers and executes modules that change the state of the servers.
		  
		  As soon as you run the ansible-playbook command, Ansible connects to the remote servers and does its thing; this lowers the risk of random servers potentially breaking whenever their scheduled tasks fail to change things successfully. The push-based approach has a significant advantage: you control when the changes happen to the servers. You do not need to wait around for a timer to expire. Each step in a playbook can target one or a group of servers. You get more work done instead of logging into the servers by hand. #spaced
		- -
	- 2. Playbooks: A Beginning
		- -
		- When the Provisioner Runs
		  The first time you run vagrant up, Vagrant will execute the provisioner and record that the provisioner was run. If you halt the virtual machine and then start it up, Vagrant remembers that it has already run the provisioner and will not run it a second time.
		  
		  You can force Vagrant to run the provisioner against a running virtual machine as follows:
		  
		  $ vagrant provision
		  You can also reboot a virtual machine and run the provisioner after reboot:
		  
		  $ vagrant reload --provision
		  Similarly, you can start up a halted virtual machine and have Vagrant run the provisioner:
		  
		  $ vagrant up --provision
		  Or you can start up the virtual machine and not run the provisioner:
		  
		  $ vagrant up --no-provision
		  We use these commands quite often to run playbooks from the command line, with a tag or a limit. #spaced
		- -
	- 3. Inventory: Describing Your Servers
		- -
		- [Figure 3.2](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781098109141/files/assets/aur3_0302.png) #flashcard
			- To sum up, a playbook contains one or more plays. A play associates an unordered set of hosts with an ordered list of tasks. Each task is associated with exactly one module. Figure 3-2 depicts the relationships between playbooks, plays, hosts, tasks, and modules.
		- -
	- 4. Variables and Facts
		- -
		- If the inventory file is marked executable, Ansible will assume it is a dynamic inventory script and will execute the file instead of reading it. #spaced
		- -